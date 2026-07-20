# Update Webhook with Locu

Updates an existing webhook in Locu.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/webhooks/:id`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [Update Webhook](https://locu.app/api/docs#tag/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Webhook ID to update. |
| `url` | body | `string` | no | New webhook destination URL. |
| `isActive` | body | `boolean` | no | Enable or disable the webhook. |
