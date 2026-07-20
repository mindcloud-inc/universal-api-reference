# List Customers by Email with Customer.io

Finds customers in Customer.io by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/customers`
- **Base URL:** `https://api.customer.io`
- **Official documentation:** [List Customers by Email](https://docs.customer.io/integrations/api/app/#tag/Customers/operation/getPeopleEmail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | The email address to search for. |
