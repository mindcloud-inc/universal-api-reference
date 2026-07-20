# Create Customer with Escrow.com

Creates a new customer in Escrow.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/customer`
- **Base URL:** `https://api.escrow-sandbox.com/2017-09-01`
- **Official documentation:** [Create Customer](https://www.escrow.com/api/docs/create-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Customer email address. |
| `first_name` | body | `string` | yes | Customer first name. |
| `last_name` | body | `string` | yes | Customer last name. |
| `phone_number` | body | `string` | no | Customer phone number. |
