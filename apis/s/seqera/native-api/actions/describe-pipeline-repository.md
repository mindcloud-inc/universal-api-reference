# Describe Remote Pipeline Repository with Seqera

Retrieves remote pipeline repository details from Seqera.

## Endpoint

- **Method:** `GET`
- **Path:** `/pipelines/info`
- **Base URL:** `https://api.cloud.seqera.io`
- **Official documentation:** [Describe Remote Pipeline Repository](https://cloud.seqera.io/openapi/seqera-api-latest.yml)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `mainScript` | query | `string` | no |
| `name` | query | `string` | no |
| `revision` | query | `string` | no |
| `workspaceId` | query | `number` | no |
