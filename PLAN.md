# Bootstrap App Plan

Original plan was to follow this resource: https://medium.com/@franciscopa91/how-to-implement-oidc-authentication-with-react-context-api-and-react-router-205e13f2d49

However, the library he uses ([oidc-client-js](https://github.com/IdentityModel/oidc-client-js)) is written in JavaScript. We definitely want to use TypeScript. oidc-client-js is no longer maintained, but points to [oidc-client-ts](https://github.com/authts/oidc-client-ts)

Option 1: oidc-client-ts looks like a good fit, and their parent repository ([authts](https://github.com/authts)) provides a [react-oidc-context](https://github.com/authts/react-oidc-context) example / starter that looks perfect for our use.

Option 2: I also found [@axa-fr/react-oidc-context](https://github.com/AxaGuilDEv/react-oidc/tree/master/packages/context) through the `oidc-client-js` documentation (it mentioned this project as an example, but they have since updated to a new OIDC client) which looks like a really advanced implementation that uses a Service Worker for added security.

**Suggested Approach**
1. CRA create-react-app to bootstrap the base application (done)
2. Start with `option 1` and get that working via React Context
3. Assuming we get it working, publish to npm and start building our own login manager on top
4. Iterate as required to have enough features to support our own needs, assuming that should be good enough for other apps
