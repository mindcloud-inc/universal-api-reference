# Create Customer with AdvantShop

Creates a new customer in AdvantShop.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/add`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Customer](https://www.advantshop.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FirstName` | body | `string` | no | Customer first name. |
| `LastName` | body | `string` | no | Customer last name. |
| `Email` | body | `string` | no | Customer email address. |
| `Phone` | body | `string` | no | Customer phone number. |
