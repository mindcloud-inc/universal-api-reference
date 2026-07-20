# Create a Webhook with WhautoChat

Creates a new webhook in WhautoChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/webhooks`
- **Base URL:** `https://api.whauto.chat`
- **Official documentation:** [Create a Webhook](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/webhooks/#2-create-a-webhook)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | no |
| `serverUrl` | body | `string` | no |
| `active` | body | `boolean` | no |
| `events[]` | body | `array<string>` | no |
| `createdAt` | body | `string` | no |
| `updatedAt` | body | `date` | no |
