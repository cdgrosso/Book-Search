# 📚 Book Search Engine — GraphQL Refactor

A full-stack application that allows users to search for books using the Google Books API and save their favorite titles. This version replaces the RESTful API with a GraphQL/Apollo Server implementation.

## 🚀 Technologies Used

- **Frontend:** React, TypeScript, Apollo Client, Bootstrap
- **Backend:** Node.js, Express, Apollo Server, GraphQL, MongoDB (via Mongoose)
- **Authentication:** JWT-based Auth with Apollo context middleware

## 📦 Features

- Search for books from Google Books API
- Save or delete books from your user profile
- Secure login and signup
- Persistent user state with JWT tokens
- GraphQL queries and mutations instead of REST

## 📁 Folder Structure

```
client/
  └── src/
      ├── pages/
      │   ├── SearchBooks.tsx
      │   └── SavedBooks.tsx
      ├── utils/
      │   ├── queries.js
      │   └── mutations.js
server/
  └── src/
      ├── schemas/
      │   ├── typeDefs.js
      │   └── resolvers.js
      └── utils/
          └── auth.js
```

## 🔑 GraphQL API Overview

### Queries
```graphql
query Me {
  me {
    _id
    username
    email
    savedBooks {
      bookId
      title
      authors
      description
    }
  }
}
```

### Mutations
```graphql
mutation login($email: String!, $password: String!) { ... }
mutation addUser($username: String!, $email: String!, $password: String!) { ... }
mutation saveBook($input: BookInput!) { ... }
mutation removeBook($bookId: String!) { ... }
```

## 🛠️ Getting Started

1. Install server and client dependencies:
```bash
npm install     # in both /client and /server directories
```

2. Add your MongoDB URI and JWT secret to a `.env` file in `/server`.

3. Run the app:
```bash
# From project root
npm run develop
```

## 🌐 Deployment

- [x] Apollo Server with GraphQL endpoint `/graphql`
- [x] MongoDB Atlas for database
- [x] Designed for Render deployment

---

© 2025 Christopher Del Grosso | Full-Stack Book Search App | GraphQL Edition