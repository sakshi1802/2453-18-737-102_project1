## Hospital Management System API


### Overview: 
This project is a Hospital Management System API built with Node.js and Express.js, leveraging a MongoDB database. The API manages hospital and ventilator information, allowing users to retrieve, search, update, and delete records related to hospitals and ventilators. The API is secured using middleware for token-based authentication.


### Features:
* Retrieve Hospital and Ventilator Details: Fetch comprehensive lists of hospitals and ventilators.
* Search Functionality: Search ventilators by status and hospital name, and search hospitals by name.
* Update Ventilator Information: Update the status of ventilators in the system.
* Add Ventilators: Users can add new ventilators to the system.
* Delete Ventilators: Ventilator records can be deleted by users.


### Technologies Used:
Node.js: Backend server runtime.
Express.js: Web framework for building the API.
MongoDB: NoSQL database for storing hospital and ventilator data.
Body-Parser: Middleware for handling request data.
JWT Authentication: Secures API routes using token-based authentication (middleware).


### API Endpoints:
* GET /hospitaldetails
Fetch all hospital details.
* GET /ventilatordetails
Retrieve all ventilator details.
* POST /searchventbystatus
Search for ventilators by status.
Body Parameter: status
* POST /searchventbyname
Search for ventilators by hospital name (case-insensitive).
Query Parameter: name
* POST /searchhospital
Search for hospitals by name (case-insensitive).
Query Parameter: Name
* PUT /updateventilator
Update ventilator status.
Body Parameters: ventilatorId, status
* POST /addventilatorbyuser
Add a new ventilator to the system.
Body Parameters: hId, ventilatorId, status, name
* DELETE /delete
Delete a ventilator by ID.
Query Parameter: ventilatorId


### Usage:
The API runs on port 1100.
Make sure MongoDB is running locally or update the MongoDB connection URL as needed.
The token-based middleware (middleware.checkToken) is applied to all routes to secure them. Ensure to include a valid token when making API requests.


### Database:
The API connects to a MongoDB database named Hospitalmanagement.


### Collections: 
Hospitaldetails
Ventilatordetails
