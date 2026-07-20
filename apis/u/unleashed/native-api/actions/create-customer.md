# Create Customer with Unleashed

Creates a new customer in Unleashed.

## Endpoint

- **Method:** `POST`
- **Path:** `/Customers`
- **Base URL:** `https://api.unleashedsoftware.com`
- **Official documentation:** [Create Customer](https://apidocs.unleashedsoftware.com/Customers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CustomerCode` | body | `string` | yes | Unique code for the customer. |
| `CustomerName` | body | `string` | yes | Display name for the customer. |
