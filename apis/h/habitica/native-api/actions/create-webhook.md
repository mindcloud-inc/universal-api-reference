# Create Webhook with Habitica

Creates a new webhook in Habitica.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/webhook`
- **Base URL:** `https://habitica.com/api/v3`
- **Official documentation:** [Create Webhook](https://habitica.com/apidoc/#api-Webhook-AddWebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The webhook target URL. |
| `label` | body | `string` | yes | A label for the webhook. |
