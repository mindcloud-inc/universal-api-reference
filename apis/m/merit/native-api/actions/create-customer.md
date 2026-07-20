# Create Customer with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v2/sendcustomer`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [Create Customer](https://api.merit.ee/connecting-robots/reference-manual/customers/create-customer/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | Unique customer name. |
| `NotTDCustomer` | body | `boolean` | yes | For Estonia, true for physical persons and foreign companies. |
| `CountryCode` | body | `string` | yes | Two-letter country code required when adding a customer. |
| `Email` | body | `string` | no | Customer email address. |
