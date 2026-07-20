# Update Document Created Webhook with Paperless

## Endpoint

- **Method:** `PATCH`
- **Path:** `/webhooks/:id`
- **Base URL:** `https://app.paperless.io/api/v1`
- **Official documentation:** [Update Document Created Webhook](https://developers.paperless.io/docs/api/1574d17775d21-receive-data-from-document-events-in-real-time-with-webhook-subscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hook_url` | body | `string` | yes | The HTTPS endpoint that should receive Paperless webhook deliveries. |
| `id` | path | `number` | yes | The Paperless webhook ID. |
| `oauth_application_id` | body | `number` | yes | The Paperless integration or OAuth application ID that owns the webhook. |
