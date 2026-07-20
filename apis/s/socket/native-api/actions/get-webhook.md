# Get Webhook with Socket

Retrieves a configured webhook from Socket.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_slug/webhooks/:webhook_id`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Get Webhook](https://docs.socket.dev/reference/getorgwebhook)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `webhook_id` | path | `string` | yes |
