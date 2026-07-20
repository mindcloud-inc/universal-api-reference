# Delete Webhook with Habitica

Deletes an existing webhook from Habitica.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/user/webhook/:id`
- **Base URL:** `https://habitica.com/api/v3`
- **Official documentation:** [Delete Webhook](https://habitica.com/apidoc/#api-Webhook-UserDeleteWebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Habitica webhook ID. |
