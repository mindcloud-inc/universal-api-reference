# Delete a project with Xata

## Endpoint

- **Method:** `DELETE`
- **Path:** `/organizations/:organizationID/projects/:projectID`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Delete a project](https://xata.io/docs/api-reference/projects/delete-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | Unique identifier of the organization containing the project |
| `projectID` | path | `string` | yes | Unique identifier of the project to delete |
