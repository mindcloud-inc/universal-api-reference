# Update Webhook with WebChange Detector

Updates an existing webhook in WebChange Detector.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/webhooks/:id`
- **Base URL:** `https://api.webchangedetector.com`
- **Official documentation:** [Update Webhook](https://api.webchangedetector.com/docs#webhook-PUTapi-v2-webhooks--id-)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `url` | body | `string` | yes |
