# Update Customer with Unleashed

Updates an existing customer in Unleashed.

## Endpoint

- **Method:** `POST`
- **Path:** `/Customers/:customerGuid`
- **Base URL:** `https://api.unleashedsoftware.com`
- **Official documentation:** [Update Customer](https://apidocs.unleashedsoftware.com/Customers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerGuid` | path | `string` | yes | The Unleashed customer GUID. |
| `CustomerCode` | body | `string` | yes | Customer code required by the Unleashed update contract. |
| `CustomerName` | body | `string` | no | Updated display name for the customer. |
| `Obsolete` | body | `boolean` | no | Marks the customer obsolete for cleanup. |
