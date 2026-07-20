# Create Webhook with Hedy

Creates a new webhook in Hedy.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.hedy.bot/webhooks`
- **Base URL:** `https://api.hedy.bot`
- **Official documentation:** [Create Webhook](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | HTTPS URL that will receive webhook events. |
| `event` | body | `string` | no | Single event to subscribe to. |
| `events` | body | `list<string>` | no | Array of events to subscribe to. Send multiple values as a array. |
