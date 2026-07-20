# Create Webhook with Court Drive

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://v1.courtapi.com`
- **Official documentation:** [Create Webhook](https://www.courtapi.com/docs/playground)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endpoint_url` | body | `string` | yes | Webhook endpoint URL to receive CourtAPI events. |
| `subscribed_events[]` | body | `array<string>` | yes | List of CourtAPI event names to subscribe the webhook to. |
