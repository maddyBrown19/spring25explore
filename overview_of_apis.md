# Overview of APIs

**Source:** [This Postman article](https://www.postman.com/what-is-an-api/) is very informative.

- API = Application Programming Interface
- A set of protocols that enable different software components to communicate and transfer data
- Side note: Amazon Simple Storage (S3) is a basic storage service in which resources are accessible via API and CLI (Command Line Interface)
- APIs share data between applications, systems, and devices through a request and response cycle - the request is sent to the API, which retrieves the data and returns it to the user
    - (1) API client
        - Starts the process by sending the request to the API server
        - Examples of triggering an API request: entering a search term, clicking a button, receiving a notification from another application
    - (2) API request
        - Endpoint - a dedicated URL that provides access to a specific resource (i.e. the endpoint /articles in a blogging app would include the logic for processing all requests that are related to articles)
        - Method – indicates the type of operation the client would like to perform on a given resource. REST APIs are accessible through standard HTTP methods that do actions like retrieving, creating, updating, and deleting data
        - Parameters – the variables that are passed to an API endpoint to provide specific instructions for the API to process. These parameters can be included in the API request as part of the URL, in the query string, or in the request body
            - Parameters in the URL come after the ; character while parameters in the query string come after the ? character (which comes after the URL)
            - <scheme>://<username>:<password>@<host>:<port>/<path>;<parameters>?<query>#<fragment>
        - Request headers – key-value pairs that provide extra details about the request, such as its content type or authentication details
        - Request body – The main part of the request, includes the actual data that is required to create, update, or delete a resource (i.e. if you were creating a new article in a blogging app, the request body would likely include the article’s content, title, and author)
    - (3) API server
        - Responsible for handling authentication, validating input data, and retrieving or manipulating data
    - (4) API response
        - The API server sends a response to the client. The response contains these components:
            - Status code – HTTP status codes are 3 digit codes that indicate the outcome of an API request. Common status codes are:
                - 200 OK = server successfully returned the requested data
                - 201 Created = server successfully created a new resource
                - 404 Not Found = server could not find the requested resource
            - Response headers – Very similar to request headers, but used to provide additional information about the server’s response
            - Response body – Includes the actual data or content the client asked for (or an error message if something went wrong)
- Benefits of APIs
    - Automation – can be used to automate repetitive, time-consuming tasks
    - Innovation – Public APIs can be used by external engineering teams, so developers can repurpose existing functionality = innovation
    - Security – APIs provide an extra layer of security by requiring authentication and authorization for any request to access sensitive data
    - Cost efficiency – APIs provide access to third-party tools, which avoids the expense of building complex in-house systems
- Webhooks: used to implement event-driven architectures in which API requests are automatically sent in response to event-based triggers
    - Example: a payment is made → the application can send an HTTP request to a pre-configured webhook URL with the relevant event data in the request payload
- Connection to microservices – APIs are used to implement microservice-based architectures, in which applications are built as a collection of small services that communicate with each other through private APIs

**GitHub API Tutorial:** [This is a great tutorial](https://docs.github.com/en/rest/using-the-rest-api/getting-started-with-the-rest-api?apiVersion=2026-03-10) that explains how to hit GitHub's REST API endpoints.