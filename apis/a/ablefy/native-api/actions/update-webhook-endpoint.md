# Update Webhook Endpoint with Ablefy

Updates an existing webhook endpoint in Ablefy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/webhook_endpoints/:id`
- **Base URL:** `https://api.myablefy.com`
- **Official documentation:** [Update Webhook Endpoint](https://api.myablefy.com/api/swagger_doc/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Webhook endpoint ID. |
| `name` | body | `string` | yes | — |
| `url` | body | `string` | yes | — |
| `event_form` | body | `string` | no | — |
| `event_ids[]` | body | `array<string>` | no | — |
| `request_format` | body | `string` | no | — |
