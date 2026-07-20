# Update project details with Xata

## Endpoint

- **Method:** `PATCH`
- **Path:** `/organizations/:organizationID/projects/:projectID`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Update project details](https://xata.io/docs/api-reference/projects/update-project-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | Unique identifier of the organization containing the project |
| `projectID` | path | `string` | yes | Unique identifier of the project to update |
| `name` | body | `string` | no | New name for the project |
| `configuration` | body | `object` | no | — |
