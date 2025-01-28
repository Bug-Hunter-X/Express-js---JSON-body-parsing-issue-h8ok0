# Express.js JSON Body Parsing Bug

This repository demonstrates a common bug in Express.js applications where JSON data sent in the request body is not parsed correctly. This typically happens when the `Content-Type` header is missing or incorrect in the request.

## Bug

The `bug.js` file contains an Express.js application that attempts to access the JSON data from the request body using `req.body`. However, if the client doesn't send the `Content-Type: application/json` header, the request body will be empty, resulting in `req.body` being an empty object.  This leads to errors or unexpected behavior in the application.

## Solution

The `bugSolution.js` file provides a corrected version of the application. It ensures that the JSON body is parsed correctly regardless of the presence or correctness of the `Content-Type` header. This is achieved by explicitly setting the `express.json()` middleware before the request handler.