# REST API using AWS API Gateway, Lambda, and DynamoDB via the AWS CDK
## Welcome to your CDK TypeScript project

This is a project for CDK development with TypeScript.
## Credits

This project was developed based on the tutorials by [conermurphy]

The `cdk.json` file tells the CDK Toolkit how to execute your app.

## Useful commands

* `npm run build`   compile typescript to js
* `npm run watch`   watch for changes and compile
* `npm run test`    perform the jest unit tests
* `npx cdk deploy`  deploy this stack to your default AWS account/region
* `npx cdk diff`    compare deployed stack with current state
* `npx cdk synth`   emits the synthesized CloudFormation template

## REST API Documentation

This project includes a REST API deployed on AWS API Gateway. The base URL for the API is: [https://kkni2mdte8.execute-api.us-east-1.amazonaws.com/prod/](https://kkni2mdte8.execute-api.us-east-1.amazonaws.com/prod/)

### Endpoints

#### Get All Posts

- **Endpoint**: `GET /posts`
- **Description**: Retrieve all posts.
- **Request**:
  - Headers:
    - `x-api-key`: Your API key
- **Response**:
  - Status Code: 200 OK
  - Body: Array of post objects

#### Get a Post

- **Endpoint**: `GET /posts/{id}`
- **Description**: Retrieve a specific post by ID.
- **Request**:
  - Headers:
    - `x-api-key`: Your API key
- **Response**:
  - Status Code: 200 OK
  - Body: Post object

#### Create a Post

- **Endpoint**: `POST /posts`
- **Description**: Create a new post.
- **Request**:
  - Headers:
    - `x-api-key`: Your API key
  - Body: Post object
- **Response**:
  - Status Code: 200 OK
  - Body: Success message

#### Delete a Post

- **Endpoint**: `DELETE /posts/{id}`
- **Description**: Delete a specific post by ID.
- **Request**:
  - Headers:
    - `x-api-key`: Your API key
- **Response**:
  - Status Code: 200 OK
  - Body: Success message

### Usage

1. Obtain an API key.
2. Include the API key in the headers of your requests (`x-api-key: YOUR_API_KEY`).
