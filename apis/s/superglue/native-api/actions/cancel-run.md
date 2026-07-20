# Cancel Run with Superglue

Cancels an existing run in Superglue.

## Endpoint

- **Method:** `POST`
- **Path:** `/runs/:runId/cancel`
- **Base URL:** `https://api.superglue.ai/v1`
- **Official documentation:** [Cancel Run](https://docs.superglue.cloud/api-reference/runs/cancel-a-run)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `runId` | path | `string` | yes | ID of the Superglue run to cancel. |
