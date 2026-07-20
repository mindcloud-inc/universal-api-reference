# Get project details with Xata

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationID/projects/:projectID`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Get project details](https://xata.io/docs/api-reference/projects/get-project-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | Unique identifier of the organization containing the project |
| `projectID` | path | `string` | yes | Unique identifier of the project to retrieve |
