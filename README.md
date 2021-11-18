# next-apollo-client-issue

The new SWC build system in nextjs 12 doesn't appear to work with apollo client/apollo-link

Steps to reproduce:
- npm install
- npm run dev
- should get error that "forward is not a function"

Two ways to get it to work:
1. Add a .babelrc file to opt out of SWC. I tried with one containing the following:
```
{
  "presets": ["next/babel"]
}
```
2. Install nextjs 11.1.2 and run the app


Notes: 
- All of the apollo code is in pages/index.js
- Following these apollo docs for setting graphql request headers: https://www.apollographql.com/docs/react/networking/advanced-http-networking/