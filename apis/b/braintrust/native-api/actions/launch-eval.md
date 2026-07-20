# Launch Eval with Braintrust

Launches an eval in Braintrust.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/eval`
- **Base URL:** `https://api.braintrust.dev`
- **Official documentation:** [Launch Eval](https://braintrust.dev/docs/api-reference/evals/launch-an-eval.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | Project id. |
| `data` | body | `object` | yes | Dataset rows or dataset reference. |
| `task` | body | `object` | yes | Task function identifier. |
| `scores[]` | body | `array<object>` | yes | Scoring functions. |
