# Library Management System

The Library Management System is a web application designed to help libraries manage their collection of books and user transactions efficiently. The application allows for user authentication, book management, borrowing and returning books, and more. It is built using Spring Boot for the backend and React for the frontend.

## Features

### User Roles
- **Admin**: Manages users and books, oversees the library operations.
- **Librarian**: Manages books, oversees borrowing and returning operations.
- **Member**: Borrows and returns books, views borrowing history.

### User Management
- Add, edit, delete users
- Assign roles (Admin, Librarian, Member)

### Book Management
- Add, edit, delete books
- Search and filter books

### Borrowing and Returning
- Borrow books
- Return books
- View borrowing history

### Authentication and Security
- Secure login and registration
- JWT-based authentication
- Role-based access control

## Tech Stack

### Backend
- Spring Boot
- Spring Security
- Spring Data JPA
- Hibernate
- MySQL/PostgreSQL

### Frontend
- React
- React Router
- Axios
- Redux
- Tailwind

## Database Schema

### Tables

**Users**
- `id` (Primary Key)
- `username`
- `password` (hashed)
- `role` (Admin, Librarian, Member)
- `email`
- `created_at`

**Books**
- `id` (Primary Key)
- `title`
- `author`
- `isbn`
- `published_date`
- `available_copies`
- `total_copies`

**BorrowRecords**
- `id` (Primary Key)
- `book_id` (Foreign Key referencing Books)
- `user_id` (Foreign Key referencing Users)
- `borrow_date`
- `return_date`
- `status` (borrowed, returned)

## Installation

### Prerequisites
- Java 17 or higher
- Node.js and npm
- MySQL/PostgreSQL

### Backend Setup
1. Clone the repository:
    ```bash
    git clone https://github.com/paul-murithi/Library-Management-System.git
    cd library-management-system/backend
    ```

2. Configure the database:
   - Update `application.properties` with your database configuration.

3. Build and run the Spring Boot application:
    ```bash
    ./mvnw spring-boot:run
    ```

### Frontend Setup
1. Navigate to the frontend directory:
    ```bash
    cd ../frontend
    ```

2. Install dependencies:
    ```bash
    npm install
    ```

3. Start the React application:
    ```bash
    npm start
    ```

## Usage

### Admin Flow
1. Login as Admin.
2. Manage users and assign roles.
3. Add, edit, delete books.

### Librarian Flow
1. Login as Librarian.
2. Manage book inventory.
3. Oversee borrowing and returning operations.

### Member Flow
1. Login as Member.
2. Browse and search for books.
3. Borrow and return books.
4. View borrowing history.

## API Endpoints

### User Management
- `POST /api/users` - Create a new user
- `GET /api/users` - Get all users
- `GET /api/users/{id}` - Get a user by ID
- `PUT /api/users/{id}` - Update a user
- `DELETE /api/users/{id}` - Delete a user

### Book Management
- `POST /api/books` - Add a new book
- `GET /api/books` - Get all books
- `GET /api/books/{id}` - Get a book by ID
- `PUT /api/books/{id}` - Update a book
- `DELETE /api/books/{id}` - Delete a book

### Borrowing and Returning
- `POST /api/borrow` - Borrow a book
- `POST /api/return` - Return a book
- `GET /api/borrow/history` - Get borrowing history

## Contributing

Contributions are welcome! Please follow these steps to contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Create a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any questions or feedback, please contact:
- [Paul Murithi](mailto:paulmurithi518@gmail.com)
- GitHub: [paul-murithi](https://github.com/paul-murithi)
