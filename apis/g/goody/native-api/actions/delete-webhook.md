# Delete Webhook with Goody

Deletes a webhook endpoint from Goody.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/webhooks/:id`
- **Base URL:** `https://api.ongoody.com`
- **Official documentation:** [Delete Webhook](https://developer.ongoody.com/commerce-api/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Webhook endpoint ID |
| `url` | body | `string` | no | The URL for the webhook to call. |
| `events[]` | body | `array<string>` | no | Filter the events you want to get webhooks for. Refer to the Webhooks list for the event names. |
