# List project backups with Xata

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationID/projects/:projectID/backups`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [List project backups](https://xata.io/docs/api-reference/projects/list-project-backups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | Unique identifier of the organization containing the project |
| `projectID` | path | `string` | yes | Unique identifier of the project to retrieve backups for |
