# Get branch details with Xata

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationID/projects/:projectID/branches/:branchID`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Get branch details](https://xata.io/docs/api-reference/branches/get-branch-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | Unique identifier of the organization containing the project |
| `projectID` | path | `string` | yes | Unique identifier of the project containing the branch |
| `branchID` | path | `string` | yes | Unique identifier of the branch to retrieve details for |
