# Get Webhook Event with IgniSign

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/webhooks/:webhookId/events/:eventId`
- **Base URL:** `https://api.ignisign.io`
- **Official documentation:** [Get Webhook Event](https://ignisign.io/docs/ignisign-api/webhooks/get-a-webhook-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The IgniSign webhook event ID. |
| `webhookId` | path | `string` | yes | The IgniSign webhook ID. |
