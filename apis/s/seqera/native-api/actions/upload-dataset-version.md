# Upload Dataset Version with Seqera

Uploads a new dataset version to Seqera.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspaceId/datasets/:datasetId/upload`
- **Base URL:** `https://api.cloud.seqera.io`
- **Official documentation:** [Upload Dataset Version](https://cloud.seqera.io/openapi/seqera-api-latest.yml)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `number` | yes |
| `datasetId` | path | `string` | yes |
| `header` | query | `boolean` | no |
| `file` | body | `file` | yes |
