# Delete Webhook with Socket

Deletes an existing webhook from Socket.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/orgs/:org_slug/webhooks/:webhook_id`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Delete Webhook](https://docs.socket.dev/reference/deleteorgwebhook)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `webhook_id` | path | `string` | yes |
