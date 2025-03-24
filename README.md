# Simple Users API with Node.js Express

## How to Run the App

1. **Install Dependencies**  
   Run the following command to install the required dependencies:

   ```bash
   yarn
   ```

2. **Start the Server**  
   Use the command below to start the application:

   ```bash
   yarn dev
   ```

   By default, the server will run on `http://localhost:5000`.

3. **Environment Variables**  
   Ensure you have a `.env` file with the necessary configuration, such as:
   ```
   PORT=5000
   MONGO_URI=<your-database-url>
   ```

## How the Users API Works

The Users API provides endpoints to manage user data. Below are the available routes:

### Endpoints

1. **Get a Single User**  
   **GET** `/users/:id`  
   Retrieves details of a user by their ID.

### Response Format

All responses are in JSON format. Example of a successful response:

```json
{
  "_id": "67e15a202e02b1f429976446",
  "name": "John Doe",
  "email": "johndoe@email.com",
  "age": 30
}
```

### Error Handling

If an error occurs, the API will return a JSON response with an appropriate status code and error message:

- 400 error

```json
{
  "message": "Invalid user ID"
}
```

- 404 error

```json
{
  "message": "User not found"
}
```

- 500 error

```json
{
  "message": "Server error"
}
```
