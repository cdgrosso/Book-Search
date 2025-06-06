# Book Search Engine (GraphQL Edition)

This application is a fully functioning book search engine built with the MERN stack. It allows users to search for books using the Google Books API, save favorites, and manage their reading list. This version has been refactored to use GraphQL with Apollo Server.

## 🚀 Features

- Search for books using Google Books API
- Login/Signup functionality with JWT authentication
- Save books to your profile
- View and remove saved books
- Fully integrated GraphQL API via Apollo Server
- Frontend React client using Apollo Client
- Deployed with Render & MongoDB Atlas

## 🧠 Technologies Used

- MongoDB & Mongoose
- Express.js
- React
- Node.js
- Apollo Server & Apollo Client
- GraphQL
- JWT for Authentication


## 🔐 Authentication

This app uses JWT for login/signup, and `auth.ts` middleware has been modified to support GraphQL context.

## 📡 GraphQL

### Queries
- `me`: returns logged-in user's saved books

### Mutations
- `login(email, password)`
- `addUser(username, email, password)`
- `saveBook(bookInput)`
- `removeBook(bookId)`

## 🌐 Deployment

- [Live App on Render](https://your-render-app-url.com)
- [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)

## 🧪 Usage

1. Clone the repo:
```bash
git clone https://github.com/your-username/book-search-graphql.git
cd book-search-graphql
```

2. Install dependencies:
```bash
npm install
cd client && npm install
```

3. Run development server:
```bash
npm run dev
```



© 2025 Book Search Engine | GraphQL Edition
