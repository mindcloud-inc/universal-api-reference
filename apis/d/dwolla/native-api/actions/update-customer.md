# Update Customer with Dwolla

Updates an existing customer in Dwolla.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/[:id]`
- **Base URL:** `https://api-sandbox.dwolla.com`
- **Official documentation:** [Update Customer](https://developers.dwolla.com/docs/api-reference/customers/update-a-customer)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Dwolla customer ID. |
| `firstName` | body | `string` | no | Updated customer first name |
| `lastName` | body | `string` | no | Updated customer last name |
| `email` | body | `string` | no | Updated customer email address |
