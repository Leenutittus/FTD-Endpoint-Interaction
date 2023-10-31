# FTD-Endpoint-Interaction

# Network Security System API Interaction with FastAPI

This is a FastAPI-based web application for interacting with a network security system API. It allows you to perform various operations such as getting tokens, managing network objects, port objects, access rules, and NAT policies.

## Prerequisites
Before using this application, make sure you have the following installed and configured:

1.Python 3.x: Ensure you have Python 3.x installed on your machine.

2.FastAPI: Install FastAPI by running pip install fastapi.

3.Requests library: Install the Requests library using pip install requests.

4.Cisco FDM Server: You need access to a Cisco FDM server with the appropriate permissions to manage network and security objects.

5.Python Environment: Set up a Python environment with the required libraries.

6.Authentication: Obtain a valid username and password to authenticate with the Cisco FDM server.

## Endpoints

The application provides various endpoints for interacting with the network security system API. Here is an overview:

### Get Token

- **POST /get_token**: Obtain an authentication token for accessing the Cisco FDM API.

### Network Objects

- **GET /get_network**: Retrieve network objects.
- **POST /create_network_object**: Create a new network object.
- **PUT /network-objects/{object_id}**: Update a network object.
- **DELETE /network-objects/{object_id}**: Delete a network object.

### Port Objects

- **GET /get_port-object**: Retrieve port objects.
- **POST /port-objects**: Create a new port object.
- **PUT /port-objects/{port_object_id}**: Update a port object.
- **DELETE /port-objects/{port_object_id}**: Delete a port object.

### Access Rules

- **GET /access_rules**: Get access rule parent ID.
- **GET /accesspolicy/{Parent_id}/access_rules**: Get access rules for a specific parent ID.
- **POST /accesspolicy/{Parent_id}/accessrules**: Create a new access rule.
- **PUT /accesspolicies/{access_policy_id}/accessrules**: Update an access rule.
- **DELETE /accesspolicies/{access_policy_id}/accessrules**: Delete an access rule.

### Auto NAT Policies

- **GET /nat_rules**: Get auto NAT policy parent ID.
- **POST /objectnatpolicy/{Parent_id}/objectnatrules**: Create a new auto NAT policy.
- **GET /objectnatpolicy/{Parent_id}/objectnatrules**: Get auto NAT policies for a specific parent ID.
- **PUT /objectnatpolicy/{Parent_id}/objectnatrules**: Update an auto NAT policy.
- **DELETE /objectnatpolicy/{Parent_id}/objectnatrules**: Delete an auto NAT policy.

### Manual NAT Policies

- **GET /manualnatpolicy**: Get manual NAT policy parent ID.
- **POST /manualnatpolicy/{Parent_id}/manualnatrules**: Create a new manual NAT policy.
- **GET /manualnatpolicy/{Parent_id}/manualnatrules**: Get manual NAT policies for a specific parent ID.
- **PUT /manualnatpolicy/{Parent_id}/manualnatrules**: Update a manual NAT policy.
- **DELETE /manualnatpolicy/{Parent_id}/manualnatrules**: Delete a manual NAT policy.

## Usage

1. Replace the placeholder URLs and authentication credentials with your Cisco FDM server details and credentials.

2. Customize the endpoints and data structures to suit your specific use case.

3. Ensure that you have the required permissions and access on your Cisco FDM server to create, update, or delete objects and policies.

4. Make sure your Python environment is set up correctly and the required libraries are installed.

5. Run the FastAPI application:

   ```bash
   uvicorn your_app_name:app --host 0.0.0.0 --port 8000
   ```

6. Access the API endpoints by making HTTP requests to the appropriate URLs.

7. Handle the responses and errors according to your application's requirements.
   
## Configuration
You need to configure the FDM API endpoint and authentication credentials in the config.py file. Make sure to secure your configuration and never expose sensitive data.

FDM_API_ENDPOINT = "https://your-fdm-api-endpoint"

FDM_USERNAME = "your-username"

FDM_PASSWORD = "your-password"

## Error Handling

The code includes basic error handling for HTTP responses. You can enhance error handling to suit your application's needs.

## Security Considerations

Ensure that your Cisco FDM server is properly secured and protected. Consider implementing secure practices such as using HTTPS for communication and validating inputs.

## Conclusion

This README serves as a guide to integrating your application with Cisco FDM using the provided code. Please refer to the [Cisco FDM API documentation](https://developer.cisco.com/docs/firepower/fdm/latest/api-reference/api-operations/) for further details on available API endpoints and data structures.

  
