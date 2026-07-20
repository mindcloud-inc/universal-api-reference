# Add Customer with Cryptolens

Creates a new customer in Cryptolens.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/customer/AddCustomer`
- **Base URL:** `https://api.cryptolens.io`
- **Official documentation:** [Add Customer](https://app.cryptolens.io/docs/api/v3/AddCustomer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | query | `string` | yes | The customer name. |
| `Email` | query | `string` | yes | The customer email. |
| `CompanyName` | query | `string` | yes | The customer company name. |
