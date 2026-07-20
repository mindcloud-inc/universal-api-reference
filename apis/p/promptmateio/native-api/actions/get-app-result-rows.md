# Get App Result Rows with Promptmate.io

## Endpoint

- **Method:** `GET`
- **Path:** `/app-results`
- **Base URL:** `https://api.promptmate.io/v1`
- **Official documentation:** [Get App Result Rows](https://apidoc.promptmate.io/api-5431941)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | query | `string` | yes | The Promptmate app ID whose results should be returned. |
| `jobId` | query | `string` | no | Optional Promptmate job ID to narrow the returned results. |
