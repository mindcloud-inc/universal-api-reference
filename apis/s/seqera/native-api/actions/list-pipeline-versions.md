# List Pipeline Versions with Seqera

Retrieves pipeline versions from Seqera.

## Endpoint

- **Method:** `GET`
- **Path:** `/pipelines/:pipelineId/versions`
- **Base URL:** `https://api.cloud.seqera.io`
- **Official documentation:** [List Pipeline Versions](https://cloud.seqera.io/openapi/seqera-api-latest.yml)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `isPublished` | query | `boolean` | no |
| `max` | query | `number` | no |
| `offset` | query | `number` | no |
| `pipelineId` | path | `number` | yes |
| `search` | query | `string` | no |
| `workspaceId` | query | `number` | no |
