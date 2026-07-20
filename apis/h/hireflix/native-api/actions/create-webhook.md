# Create Webhook with Hireflix

Creates a new webhook in Hireflix.

## Endpoint

- **Method:** `POST`
- **Path:** `me`
- **Base URL:** `https://api.hireflix.com`
- **Official documentation:** [Create Webhook](https://api.hireflix.com/me)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.url` | body | `string` | yes | The destination URL for webhook deliveries. |
| `variables.events` | body | `string` | no | The webhook event types to subscribe to. Send multiple values as a array. |
| `variables.external` | body | `string` | no | An optional external identifier for the webhook. |
