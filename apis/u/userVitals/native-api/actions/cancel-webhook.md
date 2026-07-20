# Cancel Webhook with UserVitals

Cancels a webhook in the roadmap API.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/cancel`
- **Base URL:** `https://app.roadmap.space/v1`
- **Official documentation:** [Cancel Webhook](https://api.roadmap.space/#cancel-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_url` | body | `string` | yes | The webhook target URL. |
