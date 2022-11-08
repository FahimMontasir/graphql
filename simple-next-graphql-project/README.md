1. yarn create next-app app-name
2. yarn add graphql apollo-server-micro micro
3. yarn add class-validator type-graphql reflect-metadata
4. goto type-graphql page and setup -> tsconfig & api/graphql
5. edit next.config to -->

```js
const nextConfig = {
  reactStrictMode: true,
  webpack: (config) => {
    if (!config.experiments) {
      config.experiments = {};
    }
    config.experiments.topLevelAwait = true;
    return config;
  },
};
```

6. add .graphqlrc.json and install graphql extension
   inside .graphalrc.json ->

```json
{
  "schema": "http://localhost:3000/api/graphql"
}
```

8. all graphql related file will be in the src folder
9. yarn add @graphql-codegen/cli @graphql-codegen/typescript
   @graphql-codegen/typescript-operations
   @graphql-codegen/typescript-graphql-request
   @graphql-codegen/typescript-react-query -D
10. create codegen.yml file in the root dir
11. setup codegen

```json
 "scripts": {
    "generate": "graphql-codegen",
  },
```

12. yarn add react-query graphql-request
13. create src/api.ts
14. setup \_app.js file
