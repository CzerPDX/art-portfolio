# art-portfolio
A repo to centralize the art portfolio repos using submodules.

# Website Structure:
Each of the following is a microservice that runs independently 
## Frontend
Uses `React` to provide user interface. Makes calls to the backend for site content.

## Backend
A `Node.js` server that handles requests and responses for the art portfolio application. Interfaces with the database and image bucket.

## Database
`PostgreSQL` database. Holds information about the url, description, and alt text of art portfolio images.

## Image Bucket
A `Node.js` server that manages `PUT` requests to upload images to the server and is the location that images will be loaded from on the frontend. Holds the art portfolio images and serves them. 

Interface somewhat mirrors the way that a developer might interface with `S3`. This makes a future refactor to use `S3` smoother as well as spreading the load of serving large images to another server.
