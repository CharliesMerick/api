"# api" 

# Charlies Merick B. Veloria 4E

## JSON POST with Database Integration


An API defines functionalities independently of their implementations, making it easier for developers to create programs by providing reusable building blocks. It enables developers to streamline complex processes with minimal code. Through API reuse, developers can bridge the gap between business requirements and IT capabilities, facilitating faster application development.


 


## API
An API defines functionalities independently of their implementations, making it easier for developers to create programs by providing reusable building blocks. It enables developers to streamline complex processes with minimal code. Through API reuse, developers can bridge the gap between business requirements and IT capabilities, facilitating faster application development.

Purpose: Enable interaction and communication between different software components or systems, allowing them to work together effectively.

Key Features:
Efficient Design Tools: User-friendly tools streamline API design and development, defining endpoints and access controls.
Cloud-Based Hosting: APIs are hosted in the cloud for scalability and security benefits.
Scalability: APIs easily adjust to changing workloads and user demands.
Robust Security: Built-in security features protect APIs from various threats.
Monitoring and Analytics: Tools provide insights into API usage for data-driven improvements.
Version Control: Manage and deploy API versions while maintaining compatibility.
Developer Portal: Discover, access, and test APIs with documentation and resources.
Rate Limiting: Enforce fair API usage through rate limits.
Authentication and Authorization: Control API access and actions with authentication and authorization mechanisms.
Integration Capabilities: Pre-built integrations simplify connections to external systems.

 


## API
Endpoints
 Accessible endpoints, their roles, and necessary inputs:

1. Endpoint: http://127.0.0.1/api/public/**
   Purpose: This endpoint is used to insert new data into the database.
   Required Inputs: It requires the "First name" and "Last name" parameters for data insertion.

2. Endpoint: http://127.0.0.1/api/public/postUpdate**
   Purpose: This endpoint is utilized to update existing entries in the database.
   Required Inputs: It mandates the "ID," "First name," and "Last name" parameters for updating database records.

3. Endpoint: http://127.0.0.1/api/public/postPrint**
   Purpose: This endpoint is employed to retrieve and display data stored in the database.
   Required Inputs: It does not necessitate any input parameters for data retrieval.

4. Endpoint: http://127.0.0.1/api/public/postDelete**
   Purpose: This endpoint is created for deleting specific data from the database.
   Required Inputs: It requires the "ID" parameter to identify and delete the targeted data.


 


## Request Payload

## JSON Payload postName:
{
  "lname":"hortizuela",
   "fname":"manny"
}


In this payload, used for creating a new name entry. Both "lname" and "fname" fields are present, and it appears that both fields are required as they are providing information about a person's first and last name.


## JSON Payload getName:

The provided payload lacks defined fields. While it could potentially serve the purpose of retrieving or printing a name from the system, the payload itself does not outline any mandatory or discretionary fields.

## JSON Payload updateName:
- Request payload:
{
  "id": 1,
  "lname": "wick",
  "fname": "john"
}

This payload serves the purpose of updating an already existing name entry, with the "id" parameter specifying the target entry. To complete the update, it necessitates providing the updated last name ("lname") and first name ("fname") for the person.

## Request Payload deleteName:

- Response payload:
{
  "id": 1
}

This payload is designed for the purpose of removing a name entry, and it only requires the inclusion of the unique identifier ("id") of the entry to be deleted.



## Response

## Json Payload postName:
- Response payload:
{
  "status": "success",
  "data": null
}

The "status" field signifies the status of the API request, with "success" in this instance indicating a successful request. Meanwhile, the "data" field is included but set to null, indicating that no specific data is returned for successful postName requests.

## Json Payload getName:
- Response payload:
{
  "status": "success",
  "data": [
    {"lname": "hortizuela", "fname": "manny"},
    {"lname": "licayan", "fname": "arnold"}
  ]
}

The "status" field indicates the success of the API request. It's set to "success," signifying a successful request. 

The "data" field is an array containing objects, each representing a name entry. Each object includes "lname" (last name) and "fname" (first name) fields with their respective values. This response includes multiple name entries.
 
## Json Payload updateName:
- Response payload:
{
  "status": "success",
  "data": null
}

The "status" field indicates the status of the API request, with "success" signaling a successful request.

The "data" field is included in the response but set to null, indicating that no specific data is returned for successful updateName requests.

## Json Payload deleteName:
- Response payload:
{
  "status": "success",
  "data": null
}

The "status" field denotes the status of the API request, and it's set to "success," signifying a successful request.

The "data" field is present in the response but is set to null, indicating that no specific data is returned for successful deleteName requests.


## Usage

Using Postman:

Make sure you have Postman installed and running on your computer.

Adding Data with a POST Request:
To insert data into the database through the /api/public/postName endpoint:

1. Select the POST HTTP method.
2. Input the URL: http://127.0.0.1/api/public/postName.
3. In the request body, provide values for the "fname" and "lname" parameters.
4. Click "Send" to submit the request.

Updating Data with a POST Request:
To modify existing database entries using the /api/public/postUpdate endpoint:

1. Choose the POST HTTP method.
2. Enter the URL: http://127.0.0.1/api/public/postUpdate.
3. Include the updated values for the "id," "fname," and "lname" parameters in the request body.
4. Click "Send" to send the request.

Displaying Data with a POST Request:
To retrieve database data using the /api/public/postPrint endpoint:

1. Utilize the POST HTTP method.
2. Specify the URL: http://127.0.0.1/api/public/postPrint.
3. Leave the request body empty, as no additional parameters are required.
4. Click "Send" to initiate the request.

Deleting Data with a POST Request:
To remove data from the database via the /api/public/postDelete endpoint:

1. Set the HTTP method to POST.
2. Input the URL: http://127.0.0.1/api/public/postDelete.
3. In the request body, provide the "id" parameter containing the ID of the data you wish to delete.
4. Click "Send" to execute the request.
 

## License

No License
 

## Contributors

Prof. Manny Hortizuela
Provided Parts:
-Codes
-Database Structure
-Payloads
-API
-Update
-Delete
-etc..



## Contact
Information for inquiries or support.

Charlies Merick B. Veloria
-akomerickveloria@gmail.com
-charliesmerick.veloria@student.dmmmsu.edu.ph
-09693571887
