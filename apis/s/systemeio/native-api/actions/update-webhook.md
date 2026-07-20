# Update Webhook with Systeme.io

Updates an existing webhook in Systeme.io.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/webhooks/:id`
- **Base URL:** `https://api.systeme.io`
- **Official documentation:** [Update Webhook](https://developer.systeme.io/reference/api_webhooks_id_patch-1)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/merge-patch+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Webhook ID |
| `name` | body | `string` | yes | Webhook name |
| `secret` | body | `string` | yes | Webhook secret |
| `subscriptions[]` | body | `array<string>` | no | Webhook subscriptions Send multiple values as a array. |
| `active` | body | `boolean` | no | Whether webhook is active |
