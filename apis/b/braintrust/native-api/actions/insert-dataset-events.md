# Insert Dataset Events with Braintrust

Creates dataset events in Braintrust.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/dataset/:dataset_id/insert`
- **Base URL:** `https://api.braintrust.dev`
- **Official documentation:** [Insert Dataset Events](https://braintrust.dev/docs/api-reference/datasets/insert-dataset-events.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset_id` | path | `string` | yes | Dataset id. |
| `events[]` | body | `array<object>` | yes | Events to insert. |
