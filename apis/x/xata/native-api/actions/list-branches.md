# List all branches with Xata

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationID/projects/:projectID/branches`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [List all branches](https://xata.io/docs/api-reference/branches/list-all-branches)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | Unique identifier of the organization containing the project |
| `projectID` | path | `string` | yes | Unique identifier of the project to list branches from |
