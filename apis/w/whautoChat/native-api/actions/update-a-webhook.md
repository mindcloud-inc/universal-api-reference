# Update a Webhook with WhautoChat

Updates an existing webhook in WhautoChat.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/webhooks/{webhookId}`
- **Base URL:** `https://api.whauto.chat`
- **Official documentation:** [Update a Webhook](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/webhooks/#3-update-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookId` | path | `string` | yes | Webhook unique ID |
| `name` | body | `string` | no | — |
| `serverUrl` | body | `string` | no | — |
| `active` | body | `boolean` | no | — |
| `events[]` | body | `array<string>` | no | — |
| `createdAt` | body | `string` | no | — |
| `updatedAt` | body | `date` | no | — |
