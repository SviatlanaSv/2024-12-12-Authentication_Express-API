# Authentication Express API with PostgreSQL

This project is an authentication system built with **Express.js**, **PostgreSQL**, and **JWT**. It allows users to register, log in, and update their details, with all data securely stored in a PostgreSQL database. The project includes automated tests using **Postman**, which are executed in **GitHub Actions** whenever changes are pushed to the repository.


---

## Features 🌟

- **User Registration**: Users can register by providing an email, surname, title, and password.
- **User Login**: After registration, users can log in with their email and password to receive a JWT token.
- **Update User Information**: Users can update their email or title by authenticating with a JWT token.
- **PostgreSQL Database**: All user data is stored in a PostgreSQL database.
- **Automated Tests**: Postman tests are run automatically using GitHub Actions to ensure the API works as expected.


---

## Technologies Used 🛠️

- **Express.js**: Framework for building the API.
- **PostgreSQL**: Relational database to store user data.
- **JWT (JSON Web Tokens)**: For secure user authentication.
- **Bcrypt**: For hashing user passwords.
- **Postman & Newman**: Used for testing the API.
- **GitHub Actions**: For automating the execution of Postman tests on every push to the repository.


---

## Installation 🏗️

To get started with this project locally, follow these steps:

1. **Clone the repository**:

```bash
git clone https://github.com/SviatlanaSv/2024-12-12-Authentication_Express-API.git
```

2. **Install dependencies**

```bash
npm install
```

3. **Set up PostgreSQL:**

- Ensure you have **PostgreSQL** installed and running if you're running the app locally (skip this step if you're using GitHub Actions for CI/CD, as the database will be set up automatically there).
- Create a database named `authentication_db` or update the connection settings in `app.js` to match your local PostgreSQL setup.

4. **Run the app:**

```bush
npm run dev
```
This will start the server on `http://localhost:3000`.


---

## API Endpoints 📝

1. **POST /register**: Registers a new user.
2. **POST /login**: Logs in and returns a JWT token.
3. **PUT /users/:id**: Updates a user's email and/or title (requires JWT token).


---

## Testing 🧪

Tests are set up using Postman and run through GitHub Actions on each push to the repository.


### Run tests locally

To run the Postman tests locally, use the following command:

```bush
npm run test
```
This will execute the Postman collection using **Newman**.


### GitHub Actions ⚙️

The GitHub Actions workflow is configured to run Postman tests automatically when changes are pushed to the `master` branch or when a pull request is created. It includes the following steps:

1. Sets up a **PostgreSQL** service for testing.
2. Installs dependencies and runs the application.
3. Executes the **Postman** tests using **Newman**.

Check the `.github/workflows/postman.yml` file for the detailed GitHub Actions setup.


---

## Example Postman Collection 📦

The Postman collection (`Authentication_database.postman_collection.json`) includes tests for the following:

- User registration.
- User login.
- JWT authentication for secured routes.

```json
{
  "message": "User registered successfully",
  "user": {
    "id": 1,
    "email": "example@example.com",
    "surname": "Marius",
    "title": "Mr",
    "created_at": "2025-01-14T12:00:00.000Z",
    "updated_at": "2025-01-14T12:00:00.000Z"
  }
}
```

---

## License 📄

This project is licensed under the MIT License

---
May your code run smoothly and your databases stay secure. ☕💻 Happy coding! 🚀
