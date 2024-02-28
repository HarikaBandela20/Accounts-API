# Retail Accounts API

This Mule project implements a RESTful API for managing retail accounts. It supports both GET and POST operations.

## Endpoints

### Get Accounts

**GET /accounts**

- **Description**: Retrieves retail accounts based on specified parameters.
- **Parameters**: 
  - **account_name**: Name of the account (optional)
  - **account_type**: Type of the account (optional, default is 'business')
  - **condition**: Condition for filtering (optional, default is 'AND')
- **Example Request**:
  ```http
  GET /accounts?account_name=John&account_type=personal&condition=OR
  ```

### Post Accounts

**POST /accounts**

- **Description**: Submits new retail accounts.
- **Example Request**:
  ```http
  POST /accounts
  ```
  - **Request Body**:
    ```json
    {
      "user_id": "123",
      "accounts": [
        {
          "id": "1",
          "name": "John's Business",
          "type": "business",
          "address": "123 Main St",
          "created_at": "2022-02-23T10:30:00Z",
          "air_miles": 500
        },
        {
          "id": "2",
          "name": "Jane's Personal",
          "type": "personal",
          "address": "456 Oak St",
          "created_at": "2022-02-23T11:45:00Z",
          "air_miles": 300
        }
      ]
    }
    ```

## How to Run

1. Download and install [Anypoint Studio](http://www.mulesoft.com/platform/studio).
2. Import this Mule project into Anypoint Studio.
3. Configure the necessary properties in the `mule-app.properties` file.
4. Run the project in Anypoint Studio or deploy it to [CloudHub](https://www.mulesoft.com/platform/cloudhub).

## Configuration

- This project uses HTTP and VM connectors. Ensure that you have the necessary configurations set in your Anypoint Studio.

## License

This project is licensed under the [MIT License](LICENSE). Please review the terms of the license before using or modifying this template.
