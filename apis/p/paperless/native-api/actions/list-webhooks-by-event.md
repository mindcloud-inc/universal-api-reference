# List Webhooks By Event with Paperless

## Endpoint

- **Method:** `GET`
- **Path:** `/webhooks`
- **Base URL:** `https://app.paperless.io/api/v1`
- **Official documentation:** [List Webhooks By Event](https://developers.paperless.io/docs/api/1574d17775d21-receive-data-from-document-events-in-real-time-with-webhook-subscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | query | `string` | yes | The Paperless webhook event to filter by. |
| `oauth_application_id` | query | `number` | yes | The Paperless integration or OAuth application ID for webhook subscriptions. |
