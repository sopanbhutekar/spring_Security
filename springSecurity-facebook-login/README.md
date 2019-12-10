# Implementing login with Facebook and Github 
Implementing Using Spring Security Annotation, @EnableOauth2sso which basically take care of everything.
We need to provide configuration in application.properties or application.yml file.

# 1. please create developer account on Github and FB and get App ID and Secret code which we can use in Program
# 2. Sample Config for Github
# application.yml
github:
  client:
    clientId: bd1c0a783ccdd1c9b9e4
    clientSecret: 1a9030fbca47a5b2c28e92f19050bb77824b5ad1
    accessTokenUri: https://github.com/login/oauth/access_token
    userAuthorizationUri: https://github.com/login/oauth/authorize
    clientAuthenticationScheme: form
  resource:
    userInfoUri: https://api.github.com/user

# 3. Sample Config for Facebook
# application.yml	
security:
  oauth2:
    client:
      clientId: 233668646673605
      clientSecret: 33b17e044ee6a4fa383f46ec6e28ea1d
      accessTokenUri: https://graph.facebook.com/oauth/access_token
      userAuthorizationUri: https://www.facebook.com/dialog/oauth
      tokenName: oauth_token
      authenticationScheme: query
      clientAuthenticationScheme: form
    resource:
      userInfoUri: https://graph.facebook.com/me
 


