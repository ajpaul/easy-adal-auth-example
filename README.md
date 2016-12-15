# easy-adal-auth-example with Azure AD
This is a very basic way to use ADAL.js to authenticate a user against an Azure AD using only JavaScript. I used this as a PoC for authenticating an Angular2 app and an Aurelia app to prove that we could successfully authenticate against an Azure AD, despite challenges with Azure and SPA frameworks.

## Directions

1. In Azure's portal, make a new web application. 
2. Then using that URI, register that application with your Azure AD of your choice. 
3. Specify the sign-on URI and the reply URL (for this example, your-app-name.azurewebsites.net/auth.html can be both)
4. Paste the AD name into the config.tenant part on line 42 of auth.html
5. Paste the client ID guid into config.clientId on line 43 of auth.html

If you want to redirect to a certain URL, add that URL to the reply address and edit line 52.

## Using the App

In order to use this test app, you first need to click the login button. This will take you to the Azure AD sign on screen where you will enter your credentials, which will be authenticated against the Azure AD that you registered the application with. If the process is successful, you'll get redirected back to the URL you came from. Since there is a user object present in the authentication context now, you'll see a "call api" option available, along with a logout option. In order for the call API button to work, you'll need to set up CORS on your API endpoint. If the API is called successfully, the data will be displayed in the DOM.
