# Describe Dataset with Seqera

Retrieves dataset metadata from Seqera.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId/datasets/:datasetId/metadata`
- **Base URL:** `https://api.cloud.seqera.io`
- **Official documentation:** [Describe Dataset](https://cloud.seqera.io/openapi/seqera-api-latest.yml)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `attributes` | query | `string` | no |
| `datasetId` | path | `string` | yes |
| `workspaceId` | path | `number` | yes |
