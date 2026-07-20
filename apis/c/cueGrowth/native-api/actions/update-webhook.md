# Update Webhook with CueGrowth

## Endpoint

- **Method:** `PUT`
- **Path:** `/webhooks/{webhook_id}/update`
- **Base URL:** `https://api.cuegrowth.ai/public/api`
- **Official documentation:** [Update Webhook](https://cuegrowth.ai/webhooks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_id` | path | `string` | yes | ID of the webhook. |
| `name` | body | `string` | no | Name of the webhook. |
| `active` | body | `boolean` | no | Controls whether the webhook is active. |
| `url` | body | `string` | no | URL of the webhook. |
| `event_types[]` | body | `array<string>` | no | Events that trigger the webhook. |
