# Get project backup by ID with Xata

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationID/projects/:projectID/backups/:backupID`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Get project backup by ID](https://xata.io/docs/api-reference/projects/get-project-backup-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | Unique identifier of the organization containing the project |
| `projectID` | path | `string` | yes | Unique identifier of the project to retrieve backups for |
| `backupID` | path | `string` | yes | Unique identifier of the backup for the project |
