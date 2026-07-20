# Update API Webhook with Heyy

Updates an existing API webhook in Heyy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api_webhooks/:webhookId`
- **Base URL:** `https://api.heyy.io/api/v2.0/`
- **Official documentation:** [Update API Webhook](https://docs.heyy.io/api-reference/update-api-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isActive` | body | `boolean` | no | Whether the webhook is active. |
| `url` | body | `string` | no | The webhook destination URL. |
| `webhookId` | path | `string` | yes | The Heyy webhook ID. |
