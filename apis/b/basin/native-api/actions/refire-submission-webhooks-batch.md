# Refire Submission Webhooks Batch with Basin

Re-fires webhooks for multiple submissions in Basin.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/submissions/refire_webhooks`
- **Base URL:** `https://usebasin.com`
- **Official documentation:** [Refire Submission Webhooks Batch](https://usebasin.com/api_docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `submission_ids[]` | body | `array<number>` | yes | Array of submission IDs to re-fire webhooks for. |
