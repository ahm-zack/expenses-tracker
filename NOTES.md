# graphql package =>

- It is the core GraphQL implementation in **JavaScript**.
- It provides the functionality to define GraphQL schemas, parse and validate GraphQL queries, execute queries against a schema, and format responses.
- graphql is not tied to any specific server or client framework; it's a standalone library that can be used in various JavaScript environments.

# @apollo/server =>

- This package is part of the Apollo ecosystem and is used for building GraphQL servers in Node.js.
- It provides tools and utilities to create and manage GraphQL schemas, handle incoming GraphQL requests, execute queries, and send responses.
- @apollo/server is built on top of the popular express framework, making it easy to integrate GraphQL into existing Node.js web applications.
- Overall, @apollo/server simplifies the process of creating and maintaining GraphQL servers in Node.js environments.

# What is GraphQL Schema?

- A GraphQL schema is a fundamental concept in GraphQL.
- It defines the structure of the data that clients can query and the operations they can perform. A schema in GraphQL typically consists of two main parts: typeDefs and resolvers.

# What are TypeDefs? (or Type Definitions)

- Type definitions define the shape of the data available in the GraphQL API. They specify the types of objects that can be queried and the relationships between them.

# What are Resolvers?

- Resolvers are functions that determine how to fetch the data associated with each field in the schema.

## Apollo Client

- Apollo Client is a comprehensive state management library for JavaScript that enables you to manage both local and remote data with GraphQL. Use it to fetch, cache, and modify application data, all while automatically updating your UI.

# Features

- Declarative data fetching: Write a query and receive data without manually tracking loading states.
- Excellent developer experience: Enjoy helpful tooling for TypeScript, Chrome / Firefox devtools, and VS Code.
- Designed for modern React: Take advantage of the latest React features, such as hooks.
- Incrementally adoptable: Drop Apollo into any JavaScript app and incorporate it feature by feature.
- Universally compatible: Use any build setup and any GraphQL API.
- Community driven: Share knowledge with thousands of developers in the GraphQL community.

### Declarative Data Fetching

- Apollo Client handles the request cycle from start to finish, including tracking loading and error states. There's no middleware or boilerplate code to set up before making your first request, and you don't need to worry about transforming or caching responses. All you have to do is describe the data your component needs and let Apollo Client do the heavy lifting.

```jsx
function ShowDogs() {
  //  The useQuery hook supports advanced features like an optimistic UI, refetching, and pagination.
  const { loading, error, data } = useQuery(GET_DOGS);
  if (error) return <Error />;
  if (loading) return <Fetching />;

  return <DogList dogs={data.dogs} />;
}
```

### Caching a graph is not an easy task, but they have spent years solving this problem.

```jsx
import { ApolloClient, InMemoryCache } from "@apollo/client";

const client = new ApolloClient({
  cache: new InMemoryCache(),
});
```

# Installation

```bash
npm install @apollo/client graphql
```

- **@apollo/client:** This single package contains virtually everything you need to set up Apollo Client. It includes the in-memory cache, local state management, error handling, and a React-based view layer.

- **graphql:** This package provides logic for parsing GraphQL queries.

## The sequence of steps to set up the backend server from scratch:

1.  Create a new directory for the project and navigate into it.
2.  Initialize a new Node.js project using npm init.
3.  Install the necessary dependencies: apollo-server-express, graphql, and dotenv.
4.  Create backend and frontend directories.
5.  Create a new file named index.js in the backend directory.
6.  Set up the Apollo Server in index.js.
7.  Define the GraphQL schema using typeDefs and resolvers.
8.  Start the server and test the GraphQL API using Apollo Studio.
9.  Add express server to the backend.
10. Add .env file to the backend.
11. Ignore the .env file in the .gitignore file.
12. Create the models directory in the backend.
13. Create the User and other model in the models directory.
14. Setup the MongoDB
15. Connect the MongoDB to the backend server.
16. Now we will start doing the authintication and it session management using Passport.js.
17. We will use graphql-passport library from npm to integrate the Passport.js with the GraphQL.
