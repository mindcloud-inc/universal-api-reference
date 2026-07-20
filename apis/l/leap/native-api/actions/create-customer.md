# Create Customer with Leap

Creates a new customer in Leap.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers`
- **Base URL:** `https://api.jobprogress.com/api/v3`
- **Official documentation:** [Create Customer](https://docs.api.jobprogress.com/api/customer.json)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Email address for the customer. |
| `first_name` | body | `string` | yes | First name of the customer. |
| `last_name` | body | `string` | yes | Last name of the customer. |
| `note` | body | `string` | no | Internal note to store on the customer. |
| `phone_0_label` | body | `string` | yes | Label for the primary phone number, for example cell or home. |
| `phone_0_number` | body | `number` | yes | Primary phone number for the customer. |
