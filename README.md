# Overview
This project is a simple implementation of Google Sign-In flow
using minimal set of OAuth2 scopes in order to obtain basic 
user information such as name and email.

# How to run
Create a file called `.env` and enter the following information:
```
CLIENT_ID=<oauth-client-id>
CLIENT_SECRET=<oauth-client-secret>
PORT=3000
```

Run the following commands
```bash
npm install
npm start
```

# Flow
1. The Express aplication runs and the default browser is open and directed to Google Sign-In page.
1. The User enters credentials / selects an account to log in.
1. The User is redirected to the local server where the following sequence is performed:
    1. The access code contained in the query is exchanged for tokens.
    1. The ID token is used to obtain the basic user information.
    1. The response of the basic user information is returned as JSON.