# Create Webhook with Goody

Creates a webhook endpoint in Goody.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/webhooks`
- **Base URL:** `https://api.ongoody.com`
- **Official documentation:** [Create Webhook](https://developer.ongoody.com/commerce-api/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | no | The URL for the webhook to call. |
| `events[]` | body | `array<string>` | no | Filter the events you want to get webhooks for. Refer to the Webhooks list for the event names. |
