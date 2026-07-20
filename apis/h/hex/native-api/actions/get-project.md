# Get Project with Hex

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{projectId}`
- **Base URL:** `https://app.hex.tech/api/v1`
- **Official documentation:** [Get Project](https://learn.hex.tech/docs/api-integrations/api/reference#operation/GetProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Unique ID for a Hex project. |
| `includeSharing` | query | `boolean` | no | Whether to include sharing details for the project. |
