# Create Customer with Dwolla

Creates a new customer in Dwolla.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers`
- **Base URL:** `https://api-sandbox.dwolla.com`
- **Official documentation:** [Create Customer](https://developers.dwolla.com/docs/api-reference/customers/create-a-customer)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstName` | body | `string` | yes | Customer first name |
| `lastName` | body | `string` | yes | Customer last name |
| `email` | body | `string` | yes | Customer email address |
| `type` | body | `string` | yes | Customer type |
