# Create Product with MailBluster

Creates a new product in MailBluster.

## Endpoint

- **Method:** `POST`
- **Path:** `/products`
- **Base URL:** `https://api.mailbluster.com/api`
- **Official documentation:** [Create Product](https://app.mailbluster.com/api-doc/products/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Unique product ID in MailBluster. |
| `name` | body | `string` | yes | Product name. |
