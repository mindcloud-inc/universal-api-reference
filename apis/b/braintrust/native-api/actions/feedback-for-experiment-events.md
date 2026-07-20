# Feedback For Experiment Events with Braintrust

Creates feedback for experiment events in Braintrust.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/experiment/:experiment_id/feedback`
- **Base URL:** `https://api.braintrust.dev`
- **Official documentation:** [Feedback For Experiment Events](https://braintrust.dev/docs/api-reference/experiments/feedback-for-experiment-events.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `experiment_id` | path | `string` | yes | Experiment id. |
| `feedback[]` | body | `array<object>` | yes | Feedback items. |
