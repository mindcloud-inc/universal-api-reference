# Update Customer with SmartRoutes

## Endpoint

- **Method:** `PUT`
- **Path:** `/customers/:id`
- **Base URL:** `https://api.smartroutes.io/v2`
- **Official documentation:** [Update Customer](https://api.smartroutes.io/v2/docs/api/#tag/Customers/paths/~1customers~1{id}/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the customer to update. |
| `name` | body | `string` | no | Name of the customer. |
| `account` | body | `string` | no | Account number of the customer. |
| `address` | body | `string` | no | Address of the customer. |
| `postcode` | body | `string` | no | Postcode for the customer address. |
| `lat` | body | `number` | no | Latitude of the customer location. |
| `lng` | body | `number` | no | Longitude of the customer location. |
| `phone` | body | `string` | no | Contact number of the customer. |
| `email` | body | `string` | no | Email of the customer. |
| `notes` | body | `string` | no | Notes for customer interaction. |
