# Express.js JSON Body Parsing Issue

This repository demonstrates a common issue encountered when working with JSON request bodies in Express.js applications.  The problem occurs when the client omits or incorrectly sets the `Content-Type` header, preventing Express.js from correctly parsing the JSON data.

## Bug Description

The provided `bug.js` file shows an Express.js application designed to receive JSON data via a POST request to the `/data` endpoint. However, if the client sending the request does not include the `Content-Type: application/json` header (or includes an incorrect value), the request body will be empty, leading to unexpected behavior and potential errors.

## Solution

The solution lies in configuring the body-parser middleware to handle these cases more gracefully. The `bugSolution.js` demonstrates this improved approach.