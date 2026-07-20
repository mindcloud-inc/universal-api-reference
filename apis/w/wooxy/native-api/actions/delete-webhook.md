# Delete Webhook with Wooxy

Deletes an existing webhook from Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/webhook/remove`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Delete Webhook](https://wooxy.com/api-documentation/webhooks/webhook-remove)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | Wooxy webhook ID to delete. |
