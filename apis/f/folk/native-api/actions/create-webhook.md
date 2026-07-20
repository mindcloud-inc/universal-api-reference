# Create Webhook with folk

Creates a new webhook in folk.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/webhooks`
- **Base URL:** `https://api.folk.app`
- **Official documentation:** [Create Webhook](https://developer.folk.app/api-reference/webhooks/create-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | A friendly name for the webhook. |
| `targetUrl` | body | `string` | yes | The public HTTP or HTTPS URL that receives webhook deliveries. |
| `subscribedEvents[0].eventType` | body | `string` | yes | The first subscribed webhook event type. |
| `subscribedEvents[0].filter.groupId` | body | `string` | no | Optionally limit the first subscribed event to a specific Folk group ID. |
