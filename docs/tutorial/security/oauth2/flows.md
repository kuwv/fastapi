OAuth2 can be a complex system designed to support the many possible application designs that exist. It does this through the many OAuth flows (or grant types) that are avaiable.

There are four main flows that are used widely today and are supported by OpenAPI. We'll be discussing just those.


## Password Flow (Resource Owner Credentials Grant)
The password flow is a private client that is designed to exhange a users credentials for an access token. It is usefull for applications where the login and application are the same system. The downside of using this flow is that it uses passwords which offsets the main benefit of using OAuth. This flow is usefull for internally hosted applications that provide UI and API access.


## Authorization Code Flow
The authorization code flow is the most used OAuth flow. It works in tandem with a client to redirect users to an authorization server. Once authenticated, users are then redirected back to the protected resource. This flow is popular because moved user management to an external system. This system can either be a local to the environment or an external identity provider such as Google, Facebook or Twitter. Use this along with your identity provider(s) of choice to provide access to you application from the web.


## Client Credentials Flow
The client credentials flow is designed to allow clients to connect securely to each other. There are no users in this flow and is entirely used for service accounts. This flow is usefull in microservice architectures where services need to interconnect. (Not supported)


## Implicit Flow
The implicit flow is used for public clients that are unable to authenticate. It allows a client interact with other OAuth2 protected resources without credentials and is less secure. It is typically used with single-page applications (SPA) written in JavaScript. It is not recommended for use now that all browsers support JS modules. Use this only if you must support legacy browsers. (Not supported)
