# Update Webhook with Habitica

Updates an existing webhook in Habitica.

## Endpoint

- **Method:** `PUT`
- **Path:** `/user/webhook/:id`
- **Base URL:** `https://habitica.com/api/v3`
- **Official documentation:** [Update Webhook](https://habitica.com/apidoc/#api-Webhook-UserUpdateWebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Habitica webhook ID. |
| `url` | body | `string` | no | Updated webhook target URL. |
| `label` | body | `string` | no | Updated webhook label. |
