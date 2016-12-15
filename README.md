# easy-adal-auth-example
This is a very basic way to use ADAL.js to authenticate a user against an Azure AD using only JavaScript. I used this as a PoC for authenticating an Angular2 app and an Aurelia app to prove that we could successfully authenticate against an Azure AD, despite challenges with Azure and SPA frameworks.

## Directions

1. In Azure's portal, make a new web application. 
2. Then using that URI, register that application with your AD of your choice. 
3. Specify the sign-on URI and the reply URL (for this example, your-app-name.azurewebsites.net/auth.html can be both)
4. Paste the AD name into the config.tenant part on line 38 of auth.html
5. Paste the client ID guid into config.clientId on line 39 of auth.html
6. Paste your post-logout URI (or don't...it might work without it) into lines 40 and 48 of auth.html
7. Post your reply URL into line 76 of auth.html (in this case it'd be your-app-name.azurewebsites.net/auth.html unless you specified something else)

The CORs endpoint and data endpoint I will get to in a later commit, but can be used to call a protected API after being authenticated.
