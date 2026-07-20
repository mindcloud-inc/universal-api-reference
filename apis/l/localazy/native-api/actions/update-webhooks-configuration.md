# Update Webhooks Configuration with Localazy

Updates webhook endpoints for a Localazy project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/webhooks`
- **Base URL:** `https://api.localazy.com`
- **Official documentation:** [Update Webhooks Configuration](https://localazy.com/docs/api/webhooks-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Localazy project identifier or slug. |
| `items[]` | body | `array<object>` | yes | Webhook definitions to store for the project. |
| `items[].enabled` | body | `boolean` | yes | Whether the webhook is enabled. |
| `items[].customId` | body | `string` | no | Custom identifier sent with webhook deliveries. |
| `items[].description` | body | `string` | no | Webhook description. |
| `items[].url` | body | `string` | yes | Destination URL for webhook deliveries. |
| `items[].events[]` | body | `array<string>` | yes | Webhook event identifiers to subscribe to. |
