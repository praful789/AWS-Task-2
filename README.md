# My AWS Lambda Function

This repository contains the source code and Dockerfile for an AWS Lambda function written in Python.

## Function Description

The Lambda function, defined in `myfunction.py`, is a basic example that prints "Hello World!" and logs the received event when invoked. The function returns a response with a 'statusCode' of 200.

## Dockerfile

The Dockerfile is provided to build a Lambda-compatible Docker image. It uses the official Lambda Python 3.8 base image and installs dependencies from the `requirements.txt` file.

## Usage

### Local Development

1. Clone this repository:

    ```bash
    git clone https://github.com/your-username/your-repository.git
    cd your-repository
    ```

2. Build the Docker image:

    ```bash
    docker build -t my-lambda-function .
    ```

3. Run the Lambda function locally (for testing purposes):

    ```bash
    docker run -p 9000:8080 my-lambda-function
    ```

4. Test the function using cURL or an HTTP client:

    ```bash
    curl -XPOST "http://localhost:9000/2015-03-31/functions/function/invocations" -d '{}'
    ```

### Deployment to AWS Lambda

1. Build and push the Docker image to your Amazon ECR repository:


2. Create or update your Lambda function on the AWS Management Console, specifying the ECR image URI as the container image.


3. Configure and test the Lambda function as needed.

## Author

- Praful Bhalerao
