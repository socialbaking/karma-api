# vouch-api

Vercel deployment repository of [vouch](https://github.com/socialbaking/vouch)

See [api/index.js](api/index.js) for the usage of [@socialbaking/vouch](https://www.npmjs.com/package/@socialbaking/vouch)

Vercel supports just a single function to be the default export, which is used
as a request handler. 

The vouch package passes this through internal middleware such as authentication, 
opentelemetry, and parsing, which is then routed to the correct route handler.

There is a catch all request re-write in [vercel.json](vercel.json) that vercel uses to redirect requests to this handler.