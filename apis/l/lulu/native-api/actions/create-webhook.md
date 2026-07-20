# Create Webhook with Lulu

Creates a new webhook in Lulu.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Create Webhook](https://api.lulu.com/docs/#tag/Webhooks/operation/subscribe-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topics[]` | body | `array` | yes | List of Lulu webhook topics to subscribe to. |
| `url` | body | `string` | yes | Destination URL for Lulu webhook deliveries. |
