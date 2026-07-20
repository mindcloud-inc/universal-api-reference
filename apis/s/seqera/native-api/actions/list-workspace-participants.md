# List Workspace Participants with Seqera

Retrieves workspace participants from Seqera.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:orgId/workspaces/:workspaceId/participants`
- **Base URL:** `https://api.cloud.seqera.io`
- **Official documentation:** [List Workspace Participants](https://cloud.seqera.io/openapi/seqera-api-latest.yml)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `max` | query | `number` | no |
| `offset` | query | `number` | no |
| `orgId` | path | `number` | yes |
| `search` | query | `string` | no |
| `workspaceId` | path | `number` | yes |
