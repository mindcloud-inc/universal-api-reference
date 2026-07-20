# Describe Pipeline Launch with Seqera

Retrieves pipeline launch details from Seqera.

## Endpoint

- **Method:** `GET`
- **Path:** `/pipelines/:pipelineId/launch`
- **Base URL:** `https://api.cloud.seqera.io`
- **Official documentation:** [Describe Pipeline Launch](https://cloud.seqera.io/openapi/seqera-api-latest.yml)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `pipelineId` | path | `number` | yes |
| `sourceWorkspaceId` | query | `number` | no |
| `versionId` | query | `string` | no |
| `workspaceId` | query | `number` | no |
