# Create Customer with Stax

Creates a customer in Stax.

## Endpoint

- **Method:** `POST`
- **Path:** `/customer`
- **Base URL:** `https://apiprod.fattlabs.com`
- **Official documentation:** [Create Customer](https://docs.staxpayments.com/reference/create-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Customer email |
| `firstname` | body | `string` | no | Customer first name |
| `lastname` | body | `string` | no | Customer last name |
