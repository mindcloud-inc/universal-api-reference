# Update a Webhook Endpoint with WorkOS

Updates a webhook endpoint in your WorkOS environment.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/webhook_endpoints/{id}`
- **Base URL:** `https://api.workos.com`
- **Official documentation:** [Update a Webhook Endpoint](https://workos.com/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the Webhook Endpoint. |
| `endpoint_url` | body | `string` | no | The HTTPS URL where webhooks will be sent. |
| `status` | body | `string` | no | Whether the Webhook Endpoint is enabled or disabled. |
| `events` | body | `list<string>` | no | The events that the Webhook Endpoint is subscribed to. |
