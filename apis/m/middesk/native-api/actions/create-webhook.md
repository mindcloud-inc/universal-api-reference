# Create a webhook with Middesk

Creates a webhook in your Middesk account.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Create a webhook](https://docs.middesk.com/reference/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `enabled_events[]` | body | `array` | yes | Events to subscribe the webhook to. |
| `url` | body | `string` | yes | Destination URL for webhook deliveries. |
