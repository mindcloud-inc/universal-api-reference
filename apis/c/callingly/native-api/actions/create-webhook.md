# Create Webhook with Callingly

Creates a webhook in Callingly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/webhooks`
- **Base URL:** `https://api.callingly.com`
- **Official documentation:** [Create Webhook](https://help.callingly.com/article/38-callingly-api-documentation#Create-a-Webhook-fv07m)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `event` | body | `string` | yes |
| `target_url` | body | `string` | yes |
| `call_direction` | body | `string` | no |
| `call_status` | body | `string` | no |
| `call_lead_status` | body | `string` | no |
| `team_id` | body | `number` | no |
| `number_id` | body | `number` | no |
| `field` | body | `string` | no |
| `filter` | body | `string` | no |
