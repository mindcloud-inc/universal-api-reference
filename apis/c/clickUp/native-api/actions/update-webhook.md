# Update Webhook with ClickUp

Update a configured webhook in ClickUp.

## Endpoint

- **Method:** `PUT`
- **Path:** `webhook/:webhook_id`
- **Base URL:** `https://api.clickup.com/api/v2/`
- **Official documentation:** [Update Webhook](https://developer.clickup.com/reference/getwebhooks)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `webhook_id` | path | `string` | yes |
| `endpoint` | body | `string` | no |
| `events` | body | `string` | no |
| `status` | body | `string` | no |
