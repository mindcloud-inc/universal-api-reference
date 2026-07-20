# Create Webhook with CueGrowth

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/create`
- **Base URL:** `https://api.cuegrowth.ai/public/api`
- **Official documentation:** [Create Webhook](https://cuegrowth.ai/webhooks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Name of the webhook. |
| `url` | body | `string` | no | URL of the webhook. |
| `event_types[]` | body | `array<string>` | no | Events that trigger the webhook. |
| `activate_immediately` | body | `boolean` | no | Activate the webhook immediately after creation. |
