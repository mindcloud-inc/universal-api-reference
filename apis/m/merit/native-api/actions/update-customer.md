# Update Customer with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v1/updatecustomer`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [Update Customer](https://api.merit.ee/connecting-robots/reference-manual/customers/update-customer/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Id` | body | `string` | yes | Customer ID from Merit docs. |
| `Email` | body | `string` | no | Customer email address. |
