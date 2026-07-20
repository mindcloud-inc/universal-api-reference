# Create Webhook with CloudConvert

Creates a webhook in your CloudConvert account.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.cloudconvert.com/v2`
- **Official documentation:** [Create Webhook](https://cloudconvert.com/docs/api-reference/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Webhook URL to send notifications to. |
| `events[]` | body | `array<string>` | yes | One or more webhook events to subscribe to. |
