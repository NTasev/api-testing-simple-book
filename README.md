📚 Simple Book API Testing Project

This is a personal API testing project based on a public API and inspired by a YouTube tutorial.
All test scenarios, validations, and documentation were built independently.

🔍 Project Overview

The Simple Book API simulates an online bookstore, allowing users to:
- Check the API status
- View available books
- Place, update, retrieve, and delete book orders
- Register an API client

This project tests the complete flow of a typical user journey from retrieving a book to placing and managing an order.

📁 Project Structure

QA-API-SimpleBook/
├── README.md
├── TestDocumentation.pdf
├── postman_collection.json

🛠️ Tools Used

- [Postman](https://www.postman.com/)
- JavaScript test scripts (`pm.test`, `pm.expect`)
- Postman environment/global variables
- Dynamic data generation (`{{$randomFullName}}`)

🔐 Authorization

Most requests require a bearer token. The token is stored as a global Postman variable:
{{accessToken}}

markdown
Copy
Edit

📌 Covered API Endpoints

| Method | Endpoint                      | Description                         |
|--------|-------------------------------|-------------------------------------|
| GET    | `/status`                    | Check if API is available           |
| GET    | `/books?type=non-fiction`    | Get list of available non-fiction books |
| GET    | `/books/:bookId`             | Get details of a specific book      |
| POST   | `/orders`                    | Place an order                      |
| GET    | `/orders/:orderId`           | Get order details                   |
| PATCH  | `/orders/:orderId`           | Update order                        |
| DELETE | `/orders/:orderId`           | Delete order                        |
| POST   | `/api-clients`              | Register a new API client           |

✅ Sample Test Case

**Test Case ID:** TC_API_001  
**Title:** Place an order for a non-fiction book  
**Steps:**
1. Send a GET request to `/status`
2. Retrieve a non-fiction book from `/books?type=non-fiction`
3. Store its `bookId`
4. Place an order using `/orders`
5. Validate the response and store the `orderId`
6. Retrieve, update, and delete the order

> Full test cases can be found in `TestDocumentation.pdf`

🔗 Postman Collection

[🔗 Click here to view the Postman Collection](https://nikolaytasev.postman.co/workspace/238bbe2b-3b42-4d8f-811e-897834c78597/collection/46271497-1de59625-c9f2-4019-90f4-1f0f40c2c3e1)

🧪 Why This Project?

This project demonstrates:
- Strong understanding of RESTful APIs
- Use of dynamic and chained testing
- Clear, structured test scenarios
- Readiness for real-world API testing challenges

📬 Contact
For interview purposes or portfolio reviews, please feel free to reach out via LinkedIn or email.
