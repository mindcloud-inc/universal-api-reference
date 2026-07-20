# Create Workspace Participant with Seqera

Adds a new workspace participant in Seqera.

## Endpoint

- **Method:** `PUT`
- **Path:** `/orgs/:orgId/workspaces/:workspaceId/participants/add`
- **Base URL:** `https://api.cloud.seqera.io`
- **Official documentation:** [Create Workspace Participant](https://cloud.seqera.io/openapi/seqera-api-latest.yml)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `memberId` | body | `number` | no |
| `orgId` | path | `number` | yes |
| `teamId` | body | `number` | no |
| `userNameOrEmail` | body | `string` | no |
| `workspaceId` | path | `number` | yes |
