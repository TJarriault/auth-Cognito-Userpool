# cognito login and decode token

> Simple example with instructions how to create serverless login using AWS Cognito.

![Overview](https://github.com/TJarriault/auth-Cognito-Userpool/blob/master/img/cognito-userpool.png)

These notes aim to set up a simple cognitive authentication test. Hope you find it useful!

### Step: AWS Cognito

1. Login to AWS and navigate to Cognito service
2. Create user pool in Cognito, say: `Project_Name`
3. Collect Pool Id (needed later)
4. Define domain in Open App integration > Domain name, say: `Project_Name`
5. Navigate back to AWS Cognito
6. Create client in App clients (no secret needed)
7. Open App client settings
8. Collect app id (needed later)
9. Define callback & sign out urls. Example: https://localhost/
10. Select Allowed OAuth Flows: Authorization code grant, Implicit grant
11. Select Allowed Oauth Scopes: phone, email, openid, aws.cognito.signin.user.admin, profile

### Detail of Cognito Configuration :
![Overview](https://github.com/TJarriault/auth-Cognito-Userpool/blob/master/img/cognito-app-client.png)
![Overview](https://github.com/TJarriault/auth-Cognito-Userpool/blob/master/img/cognito-client-setting.png)
### Step: Frontend App

1. Install application sample on http server (ex : nginx / apache)
     Requirement : the URL for signin should be on HTTP#S#
2. Configure setting on the index.html
3. Acces to the web page : https://APPLI_DNS/index.html

