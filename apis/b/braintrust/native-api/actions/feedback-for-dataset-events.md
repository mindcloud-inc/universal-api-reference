# Feedback For Dataset Events with Braintrust

Creates feedback for dataset events in Braintrust.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/dataset/:dataset_id/feedback`
- **Base URL:** `https://api.braintrust.dev`
- **Official documentation:** [Feedback For Dataset Events](https://braintrust.dev/docs/api-reference/datasets/feedback-for-dataset-events.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset_id` | path | `string` | yes | Dataset id. |
| `feedback[]` | body | `array<object>` | yes | Feedback items. |
