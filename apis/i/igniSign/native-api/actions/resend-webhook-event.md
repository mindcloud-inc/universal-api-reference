# Resend Webhook Event with IgniSign

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/webhooks/:webhookId/events/:eventId/resend`
- **Base URL:** `https://api.ignisign.io`
- **Official documentation:** [Resend Webhook Event](https://ignisign.io/docs/ignisign-api/webhooks/resend-a-webhook-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The IgniSign webhook event ID. |
| `webhookId` | path | `string` | yes | The IgniSign webhook ID. |
