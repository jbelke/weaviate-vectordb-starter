# Weaviate Docker Compose & Postman Collection

## Introduction

This Postman collection is designed to help you interact with the Weaviate API, a vector database for AI-native applications. It contains various endpoints to explore the capabilities of Weaviate, such as listing available endpoints, managing schemas, and performing other key operations.

## Getting Started

Before you can use this collection, you need to configure it for your local or remote Weaviate instance.

### Base Path

The base path for the Weaviate server follows this format:  
`[YOUR-WEAVIATE-HOST]:[PORT]/v1`.

For example, when running Weaviate locally, the base path would look like:
http://localhost:9080/v1

### Environment Setup

1. **Create an Environment Variable for `baseUrl`:**

   In order to use the collection effectively, you must create an environment variable called `baseUrl` in Postman:
   - Go to the **Environments** tab in Postman.
   - Click **Add** to create a new environment.
   - Add a variable named `baseUrl`.
   - Set its initial value to `http://localhost:9080/v1` (or your actual server URL if it's hosted remotely).
   
   This will allow the collection to dynamically substitute `{{baseUrl}}` in the API requests.

2. **Using Docker Compose:**

   If you’re using Docker to run Weaviate, you can easily get started by running the provided `docker-compose.yml` file. This file configures the Weaviate instance and other dependencies, and allows you to start the service quickly.

   To start Weaviate using Docker Compose:

   - Ensure Docker and Docker Compose are installed on your system.
   - Open a terminal and navigate to the directory containing the `docker-compose.yml` file.
   - Run the following command to start the Weaviate instance in detached mode:

     ```bash
     docker-compose up -d
     ```

   This command will pull the necessary images and start the containers in the background.

   - Once the containers are up and running, you can access Weaviate at `http://localhost:9080/v1`.

3. **Using the Collection:**

   Once the `baseUrl` variable is set, and Weaviate is running via Docker Compose, you can start using the requests in this collection to interact with your Weaviate instance. Each request in the collection will automatically append the correct base URL to the endpoint paths.

### Example Request

**List available endpoints:**

- **Method:** `GET`
- **URL:** `{{baseUrl}}/`
- **Description:** This request lists the available endpoints to help you navigate and discover the REST API capabilities.

## Documentation & Support

- For detailed Weaviate documentation, tutorials, and code examples, visit the [Weaviate documentation page](https://weaviate.io/developers/weaviate).
- If you encounter any issues or have questions, please join the community forum at [https://forum.weaviate.io/](https://forum.weaviate.io/).
- You can report bugs or request new features by opening an issue on the [Weaviate GitHub repository](https://github.com/weaviate/weaviate).
- Fun with OpenAI/ollama
(https://github.com/openai/openai-cookbook/blob/main/examples/vector_databases/weaviate/question-answering-with-weaviate-and-openai.ipynb)

## Author

Created by [jbelke](https://github.com/jbelke)
