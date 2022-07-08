[base](https://www.apollographql.com/blog/apollo-client/next-js/next-js-getting-started/)

## Setting up GraphQL

### Apollo Client

Install with reference to [here](https://www.apollographql.com/docs/react/get-started)

```sh
npm install @apollo/client graphql
```

### Codegen

#### 1. Install its CLI with reference to [here](https://www.graphql-code-generator.com/docs/getting-started/installation)

```sh
npm install -D @graphql-codegen/cli
```

#### 2. Install its plugins with reference to [here](https://www.graphql-code-generator.com/docs/guides/react#apollo-and-urql)

```sh
npm install -D @graphql-codegen/typed-document-node
npm install -D @graphql-codegen/typescript
npm install -D @graphql-codegen/typescript-operations
```

#### 3. Configure the plugin

Create or update your codegen.yaml file as follows:

```yml
schema: http://my-graphql-api.com/graphql
documents: "./src/**/*.graphql"
generates:
  ./src/generated.ts:
    plugins:
      - typescript
      - typescript-operations
      - typed-document-node
```

#### 4. Run the codegen

```sh
npx graphql-codegen
```

## Note

### GraphQL Code Generator vs [Apollo CLI](https://github.com/apollographql/apollo-tooling)

[This error](https://qiita.com/koedamon/items/0fd3a01f7e398e54b747) 😫

More error 🤯

```sh
error @apollo/federation@0.27.0: The engine "node" is incompatible with this module. Expected version ">=12.13.0 <17.0". Got "18.3.0"
error Found incompatible module.
```
