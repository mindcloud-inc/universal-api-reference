# Create a new branch from a backup of another branch with Xata

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:organizationID/projects/:projectID/branches/:branchID/restore`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Create a new branch from a backup of another branch](https://xata.io/docs/api-reference/branches/create-a-new-branch-from-a-backup-of-another-branch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | Unique identifier of the organization containing the project |
| `projectID` | path | `string` | yes | Unique identifier of the project containing the source branch |
| `branchID` | path | `string` | yes | Unique identifier of the source branch of the backup |
| `name` | body | `string` | yes | Human-readable name of the branch |
| `description` | body | `string` | no | Optional description of the branch purpose or contents |
| `scaleToZero` | body | `object` | no | — |
| `backupConfiguration` | body | `object` | no | — |
| `configuration` | body | `object` | no | — |
