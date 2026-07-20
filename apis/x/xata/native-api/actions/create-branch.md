# Create a new branch with Xata

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:organizationID/projects/:projectID/branches`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Create a new branch](https://xata.io/docs/api-reference/branches/create-a-new-branch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | Unique identifier of the organization containing the project |
| `projectID` | path | `string` | yes | Unique identifier of the project to create the branch in |
| `name` | body | `string` | yes | Human-readable name for the new branch |
| `description` | body | `string` | no | Optional description for the branch purpose or contents (max 50 characters) |
| `scaleToZero` | body | `object` | no | — |
| `backupConfiguration` | body | `object` | no | — |
| `mode` | body | `string` | yes | — |
| `parentID` | body | `string` | yes | If present, the branch will inherit the parent branch configuration and data |
| `configuration` | body | `object` | yes | — |
