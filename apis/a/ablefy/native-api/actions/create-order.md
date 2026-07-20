# Create Order with Ablefy

Creates a new order in Ablefy.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/orders`
- **Base URL:** `https://api.myablefy.com`
- **Official documentation:** [Create Order](https://api.myablefy.com/api/swagger_doc/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `product_id` | body | `number` | yes |
| `email` | body | `string` | yes |
| `first_name` | body | `string` | yes |
| `last_name` | body | `string` | yes |
| `ticket_date_id` | body | `number` | no |
| `pid` | body | `number` | no |
| `prid` | body | `number` | no |
