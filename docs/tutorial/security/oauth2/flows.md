OAuth2 is a complex security protocol designed to be flexible enough to support many possible application designs. This is possible through the many OAuth flows (or grant types) that are avaiable. There are four main flows that are used widely today and are supported by OpenAPI.


## Password Flow (Resource Owner Credentials Grant)
The password flow exhanges user credentials for an access token. It is usefull for applications where the login and application are the same system. This flow is commonly used for internally hosted applications that provide UI and API access. The downside of using this flow is that it uses passwords which offsets the main benefit of using OAuth.


## Authorization Code Flow
The authorization code flow is the most used OAuth flow. It works by redirecting a user's broser to an authorization server for authentication which then redirects the user back to the protected resource. This flow is popular because it allows systems that are already designed for authentication and authorization to be used. This can be either an off-the-self authorization server or web providers such as Google, Facebook or Twitter. Use this along with your identity provider(s) of choice to provide access to you application from the web.


## Client Credentials Flow
The client credentials flow is designed to allow clients to connect securely to each other. There are no users associated with this flow and is entirely used for service accounts. This flow is usefull in microservice architectures where services need to interconnect. (Not supported)


## Implicit Flow
The implicit flow is used for public clients that are unable to authenticate. It allows a client interact with other OAuth2 protected resources without credentials and is less secure. It is typically used with single-page applications (SPA) written in JavaScript. It is not recommended for use now that all browsers support JS modules. Use this only if you must support legacy browsers. (Not supported)
