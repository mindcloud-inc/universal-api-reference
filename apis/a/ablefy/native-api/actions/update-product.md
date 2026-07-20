# Update Product with Ablefy

Updates an existing product in Ablefy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/products/:id`
- **Base URL:** `https://api.myablefy.com`
- **Official documentation:** [Update Product](https://api.myablefy.com/api/swagger_doc/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Product ID. |
| `name` | body | `string` | yes | Product name. |
| `success_url` | body | `string` | no | — |
| `cancel_url` | body | `string` | no | — |
| `error_url` | body | `string` | no | — |
| `webhook_endpoint_ids[]` | body | `array<string>` | no | — |
| `webhook_url` | body | `string` | no | — |
| `page_header` | body | `string` | no | — |
| `page_footer` | body | `string` | no | — |
| `free` | body | `boolean` | no | — |
| `active` | body | `boolean` | no | — |
| `private` | body | `boolean` | no | — |
| `performance_period` | body | `boolean` | no | — |
| `performance_period_type` | body | `string` | no | — |
| `performance_period_text` | body | `string` | no | — |
| `form` | body | `string` | no | — |
| `webhook_endpoint_form` | body | `string` | no | — |
| `forward` | body | `object` | no | — |
| `team_members[]` | body | `array<object>` | no | — |
| `prices_attributes[]` | body | `array<object>` | no | — |
| `success_email` | body | `object` | no | — |
