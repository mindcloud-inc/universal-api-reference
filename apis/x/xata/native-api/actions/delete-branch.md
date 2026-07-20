# Delete a branch with Xata

## Endpoint

- **Method:** `DELETE`
- **Path:** `/organizations/:organizationID/projects/:projectID/branches/:branchID`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Delete a branch](https://xata.io/docs/api-reference/branches/delete-a-branch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | Unique identifier of the organization containing the project |
| `projectID` | path | `string` | yes | Unique identifier of the project containing the branch |
| `branchID` | path | `string` | yes | Unique identifier of the branch to delete |
