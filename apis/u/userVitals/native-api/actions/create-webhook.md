# Create Webhook with UserVitals

Creates a new webhook in the roadmap API.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://app.roadmap.space/v1`
- **Official documentation:** [Create Webhook](https://api.roadmap.space/#create-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | body | `string` | yes | The webhook event. |
| `target_url` | body | `string` | yes | The webhook target URL. |
