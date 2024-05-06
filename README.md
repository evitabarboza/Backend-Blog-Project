# Backend-Blog

This project is a backend API for managing authors and their blogs. It includes schemas for authors and blogs, along with POST and GET methods to store and fetch data. MongoDB is used for data storage.

### Installation

To install the necessary dependencies, use the following command:

```
npm install
```

### Usage

To start the server, run:

```
npm start
```

### API Endpoints

1. **POST /api/author**
   - Creates a new author.
   - Request Body:
     ```json
     {
       "name": "John Doe",
       "email": "john@example.com",
       "publishedDate": "2024-05-10"
     }
     ```
   - Response:
     ```json
     {
       "message": "Author created successfully",
       "author": {
         "_id": "609abc123def456789012345",
         "name": "John Doe",
         "email": "john@example.com",
         "publishedDate": "2024-05-10"
       }
     }
     ```

2. **GET /api/author**
   - Retrieves all authors.
   - Response:
     ```json
     [
       {
         "_id": "609abc123def456789012345",
         "name": "John Doe",
         "email": "john@example.com",
         "publishedDate": "2024-05-10"
       },
       {
         "_id": "609def456ghi789012345678",
         "name": "Jane Smith",
         "email": "jane@example.com",
         "publishedDate": "2024-05-12"
       }
     ]
     ```

3. **POST /api/blog**
   - Creates a new blog post.
   - Request Body:
     ```json
     {
       "title": "My First Blog Post",
       "blogContent": "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
       "authorName": "John Doe"
     }
     ```
   - Response:
     ```json
     {
       "message": "Blog post created successfully",
       "blog": {
         "_id": "60abcd123456def789012345",
         "title": "My First Blog Post",
         "blogContent": "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
         "authorName": "John Doe"
       }
     }
     ```

4. **GET /api/blog**
   - Retrieves all blog posts.
   - Response:
     ```json
     [
       {
         "_id": "60abcd123456def789012345",
         "title": "My First Blog Post",
         "blogContent": "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
         "authorName": "John Doe"
       },
       {
         "_id": "60efgh456789ijk012345678",
         "title": "Introduction to MongoDB",
         "blogContent": "MongoDB is a NoSQL database.",
         "authorName": "Jane Smith"
       }
     ]
     ```

### Technologies Used

- JavaScript
- Node.js
- Express.js
- MongoDB

### Credits

This API is created by Evita Sharon Barboza. Feel free to contribute and customize it according to your needs.
