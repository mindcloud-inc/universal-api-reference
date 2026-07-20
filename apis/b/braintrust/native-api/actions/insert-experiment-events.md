# Insert Experiment Events with Braintrust

Creates experiment events in Braintrust.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/experiment/:experiment_id/insert`
- **Base URL:** `https://api.braintrust.dev`
- **Official documentation:** [Insert Experiment Events](https://braintrust.dev/docs/api-reference/experiments/insert-experiment-events.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `experiment_id` | path | `string` | yes | Experiment id. |
| `events[]` | body | `array<object>` | yes | Events to insert. |
