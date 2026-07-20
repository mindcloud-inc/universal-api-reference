# Get PostgreSQL configuration details with Xata

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationID/projects/:projectID/branches/:branchID/postgres-config`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Get PostgreSQL configuration details](https://xata.io/docs/api-reference/branches/get-postgresql-configuration-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | Unique identifier of the organization containing the project |
| `projectID` | path | `string` | yes | Unique identifier of the project containing the branch |
| `branchID` | path | `string` | yes | Unique identifier of the branch to retrieve PostgreSQL configuration for |
