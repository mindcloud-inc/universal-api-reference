# Create Webhook with Attio

Creates a webhook in Attio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/webhooks`
- **Base URL:** `https://api.attio.com`
- **Official documentation:** [Create Webhook](https://docs.attio.com/rest-api/endpoint-reference/webhooks/create-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `targetUrl` | body | `string` | yes | The HTTPS URL Attio should send webhook events to. |
| `subscriptions[]` | body | `array<object>` | yes | Webhook subscriptions array using Attio's documented event_type and optional filter objects. |
