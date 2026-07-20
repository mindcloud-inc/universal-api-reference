# Update Webhook with Lulu

Updates an existing webhook in Lulu.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/webhooks/{id}/`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Update Webhook](https://api.lulu.com/docs/#tag/Webhooks/operation/update-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Lulu webhook ID. |
| `topics[]` | body | `array` | no | Replacement Lulu webhook topic list. |
| `url` | body | `string` | no | Updated destination URL for the webhook. |
| `is_active` | body | `boolean` | no | Whether the webhook should remain active. |
