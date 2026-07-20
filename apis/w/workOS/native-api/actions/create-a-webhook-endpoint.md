# Create a Webhook Endpoint with WorkOS

Creates a webhook endpoint in your WorkOS environment.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook_endpoints`
- **Base URL:** `https://api.workos.com`
- **Official documentation:** [Create a Webhook Endpoint](https://workos.com/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endpoint_url` | body | `string` | yes | The HTTPS URL where webhooks will be sent. |
| `events` | body | `list<string>` | yes | The events that the Webhook Endpoint is subscribed to. |
