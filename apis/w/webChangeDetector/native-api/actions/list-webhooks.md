# List Webhooks with WebChange Detector

Retrieves webhooks from WebChange Detector.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/webhooks`
- **Base URL:** `https://api.webchangedetector.com`
- **Official documentation:** [List Webhooks](https://api.webchangedetector.com/docs#webhook-GETapi-v2-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | query | `list` | no | Accepted values: `batch_finished`, `comparison_status_new`, `queue_status_done`, `queue_status_failed`. |
