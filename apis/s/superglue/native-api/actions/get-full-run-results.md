# Get Full Run Results with Superglue

Retrieves full run results from Superglue.

## Endpoint

- **Method:** `GET`
- **Path:** `/runs/:runId/results`
- **Base URL:** `https://api.superglue.ai/v1`
- **Official documentation:** [Get Full Run Results](https://docs.superglue.cloud/api-reference/runs/get-full-run-results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `runId` | path | `string` | yes | ID of the Superglue run. |
| `truncate` | query | `list` | no | If true, truncate large results for preview. Accepted values: `false`, `true`. |
