# Describe Pipeline Schema with Seqera

Retrieves a pipeline schema from Seqera.

## Endpoint

- **Method:** `GET`
- **Path:** `/pipelines/:pipelineId/schema`
- **Base URL:** `https://api.cloud.seqera.io`
- **Official documentation:** [Describe Pipeline Schema](https://cloud.seqera.io/openapi/seqera-api-latest.yml)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `attributes` | query | `string` | no |
| `pipelineId` | path | `number` | yes |
| `sourceWorkspaceId` | query | `number` | no |
| `versionId` | query | `string` | no |
| `workspaceId` | query | `number` | no |
