# Update Webhook with Priority Matrix

Updates an existing webhook in Priority Matrix.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/hook/:id/`
- **Base URL:** `https://sync.appfluence.com`
- **Official documentation:** [Update Webhook](https://sync.appfluence.com/developer/guide/#webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Priority Matrix webhook ID. |
| `event` | body | `string` | no | Webhook event name. |
| `target` | body | `string` | no | Webhook target URL. |
| `enabled` | body | `boolean` | no | Whether the webhook is enabled. |
