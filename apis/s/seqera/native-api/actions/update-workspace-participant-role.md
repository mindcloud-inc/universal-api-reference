# Update Workspace Participant Role with Seqera

Updates a workspace participant role in Seqera.

## Endpoint

- **Method:** `PUT`
- **Path:** `/orgs/:orgId/workspaces/:workspaceId/participants/:participantId/role`
- **Base URL:** `https://api.cloud.seqera.io`
- **Official documentation:** [Update Workspace Participant Role](https://cloud.seqera.io/openapi/seqera-api-latest.yml)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orgId` | path | `number` | yes |
| `participantId` | path | `number` | yes |
| `role` | body | `string` | no |
| `workspaceId` | path | `number` | yes |
