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

## Authorization Code Grant Type Flow


1. The client sends a request to the provider’s authorization URL
2. The provider asks the user to authenticate
3. The provider asks the user to consent to the client acting on their behalf
4. The provider sends the client a unique authorization code
5. The client sends the authorization code back to the Provider’s token URL
6. The provider sends the Access Token, the Refresh Token and the ID token to be used with other provider URLs on behalf of the user


![image](https://user-images.githubusercontent.com/55410194/146191420-38e7baeb-269c-49d5-8acb-2649b6b09bf9.png)


