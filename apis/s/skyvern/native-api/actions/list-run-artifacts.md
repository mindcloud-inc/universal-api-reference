# List Run Artifacts with Skyvern

Retrieves artifacts for a run from Skyvern.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/runs/:run_id/artifacts`
- **Base URL:** `https://api.skyvern.com`
- **Official documentation:** [List Run Artifacts](https://www.skyvern.com/docs/api-reference/artifacts/get-artifacts-for-a-run)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `artifact_type` | query | `string` | no | Optional filter for artifacts returned by the run. |
| `run_id` | path | `string` | yes | The task run or workflow run ID. |
