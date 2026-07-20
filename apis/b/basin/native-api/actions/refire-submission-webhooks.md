# Refire Submission Webhooks with Basin

Re-fires webhooks for one submission in Basin.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/submissions/:id/refire_webhooks`
- **Base URL:** `https://usebasin.com`
- **Official documentation:** [Refire Submission Webhooks](https://usebasin.com/api_docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the submission to re-fire webhooks for. |
