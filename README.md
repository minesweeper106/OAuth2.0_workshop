# OAuth2.0 + OIDC

## Task - Implement Google Authentication in your web application

- Ability to log in user with the google credentials
- Ability to log user out
- Oauth 2.0 Authorization code flow implemented
- Client Authorization for scopes: openid, profile, email
- Ability to fetch profile data and register user into the DB

## Tokens and Artifacts

- Client Credentials – Client ID & Client Secret assigned by an OAuth Provider
- Scopes – OAuth 2.0 operates on scope authorization
- State - a client-side generated code, that needs to be stored in a session and used for validations
- Authorization code – to be exchanged for the Access token. The first step of the web flow is to request authorization from the user. This is accomplished by creating an authorization request link for the user to click on.
- ID token - user profile data, base64-encoded JSON string containing data about the user
- Access token - needs to be attached to the HTTP Authorization header to all the API calls to access data from OAuth Server
- Refresh token - to be exchanged for a new access token

## Google Auth Endpoints

- Authorization Endpoint https://accounts.google.com/o/oauth2/v2/auth
- Token Endpoint https://oauth2.googleapis.com/token
- Token Keys Endpoint https://www.googleapis.com/oauth2/v3/certs
- Token Revocation Endpoint https://oauth2.googleapis.com/revoke
- User Information Endpoint https://openidconnect.googleapis.com/v1/userinfo
- Discovery Endpoint https://accounts.google.com/.well-known/openid-configuration

## Registering a client and obtaining client credentials at a provider

In google cloud console:
1. Create new project
2. Create new Oauth Consent screen for external use
3. Create new credentials for Web Application
4. Obtain ClientID and Client Secret


## Authorization Code Grant Type Flow


1. The client sends a request to the provider’s authorization URL
2. The provider asks the user to authenticate
3. The provider asks the user to consent to the client acting on their behalf
4. The provider sends the client a unique authorization code
5. The client sends the authorization code back to the Provider’s token URL
6. The provider sends the Access Token, the Refresh Token and the ID token to be used with other provider URLs on behalf of the user


![image](https://user-images.githubusercontent.com/55410194/146191420-38e7baeb-269c-49d5-8acb-2649b6b09bf9.png)


## User Authorisation Request

![image](https://user-images.githubusercontent.com/55410194/146191878-6d4740e6-383c-4b23-a122-f760cde61507.png)

## Access Token/ID Token Request

![image](https://user-images.githubusercontent.com/55410194/146191948-7f297587-51e9-4e85-bfef-1c7fbbb49b63.png)


## Token response

![image](https://user-images.githubusercontent.com/55410194/146192008-1a7ec4fa-dd27-4813-aa69-8201f3262bd1.png)

## Useful links

- Google Cloud Console – required to create client credentials https://console.cloud.google.com/apis/dashboard
- OAuth 2.0 Playground https://www.oauth.com/playground/
- OpenID Connect Playground https://openidconnect.net
- JWT Decoder https://jwt.io
- Google OAuth 2.0 Authorisation Code Grant Instructions https://developers.google.com/identity/protocols/oauth2/openid-connect#php

## Tutorials

### PHP
- PHP example - https://www.w3jar.com/login-with-google-account-using-php-mysqli-source-code/
- PHP GAPI Library documentation - https://developers.google.com/identity/protocols/oauth2/web-server#php

### Python
- Python example https://pretagteam.com/question/using-google-oauth2-with-flask
- Python GAPI Library documentation - https://developers.google.com/identity/protocols/oauth2/web-server#python_5




