# Create Webhook with Paperless

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://app.paperless.io/api/v1`
- **Official documentation:** [Create Webhook](https://developers.paperless.io/docs/api/1574d17775d21-receive-data-from-document-events-in-real-time-with-webhook-subscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[]` | body | `array<string>` | yes | The Paperless document events to subscribe to. Send multiple values as a array. |
| `hook_url` | body | `string` | yes | The HTTPS endpoint that should receive Paperless webhook deliveries. |
| `oauth_application_id` | body | `number` | yes | The Paperless integration or OAuth application ID that owns the webhook. |
