# Update Webhook with Kiwify

Updates an existing webhook in Kiwify.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/webhooks/:id`
- **Base URL:** `https://public-api.kiwify.com`
- **Official documentation:** [Update Webhook](https://docs.kiwify.com.br/api-reference/webhooks/edit)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
| `url` | body | `string` | no |
| `products` | body | `string` | no |
| `token` | body | `string` | no |
