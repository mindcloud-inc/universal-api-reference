# Create Webhook with SafetyCulture

Creates a new webhook in SafetyCulture.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/v1/webhooks`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [Create Webhook](https://developer.safetyculture.com/reference/webhooksservice_createwebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trigger_events[]` | body | `array<string>` | yes | The list of event types to trigger the webhook. Cannot be empty. |
| `url` | body | `string` | yes | The webhook destination URL. |
