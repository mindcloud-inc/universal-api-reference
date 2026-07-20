# Update Webhook with Pipefile

## Endpoint

- **Method:** `PUT`
- **Path:** `/webhooks/:id/`
- **Base URL:** `https://api.pipefile.com/v1`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Pipefile webhook ID. |
| `event` | body | `string` | yes | Updated Pipefile event that should trigger the webhook. |
| `target` | body | `string` | yes | Updated destination URL for webhook deliveries. |
