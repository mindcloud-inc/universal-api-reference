# Create Customer with SureCart

## Endpoint

- **Method:** `POST`
- **Path:** `v1/customers`
- **Base URL:** `https://api.surecart.com`
- **Official documentation:** [Create Customer](https://developer.surecart.com/api-reference/customers/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer.email` | body | `string` | yes | The customer email address. |
| `customer.name` | body | `string` | no | The customer full name or business name. |
