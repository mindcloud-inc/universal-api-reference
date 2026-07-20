# Get Artifact with Skyvern

Retrieves a run artifact from Skyvern.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/artifacts/:artifact_id`
- **Base URL:** `https://api.skyvern.com`
- **Official documentation:** [Get Artifact](https://www.skyvern.com/docs/api-reference/artifacts/get-an-artifact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `artifact_id` | path | `string` | yes | The artifact ID to retrieve. |
