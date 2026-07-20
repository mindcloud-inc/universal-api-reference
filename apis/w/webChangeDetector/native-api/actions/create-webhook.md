# Create Webhook with WebChange Detector

Creates a new webhook in WebChange Detector.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/webhooks`
- **Base URL:** `https://api.webchangedetector.com`
- **Official documentation:** [Create Webhook](https://api.webchangedetector.com/docs#webhook-POSTapi-v2-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | body | `list` | yes | Accepted values: `batch_finished`, `comparison_status_new`, `comparison_status_new_collection`, `comparison_summary`, `queue_status_done`, `queue_status_failed`, `wordpress_cron`, `wordpress_single_call`. |
| `url` | body | `string` | yes | — |
