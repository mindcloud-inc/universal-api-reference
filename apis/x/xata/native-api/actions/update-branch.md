# Update branch details with Xata

## Endpoint

- **Method:** `PATCH`
- **Path:** `/organizations/:organizationID/projects/:projectID/branches/:branchID`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Update branch details](https://xata.io/docs/api-reference/branches/update-branch-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | Unique identifier of the organization containing the project |
| `projectID` | path | `string` | yes | Unique identifier of the project containing the branch |
| `branchID` | path | `string` | yes | Unique identifier of the branch to update |
| `name` | body | `string` | no | New name for the branch |
| `description` | body | `string` | no | New description for the branch (max 50 characters) |
| `replicas` | body | `number` | no | Number of database replicas to scale to |
| `storage` | body | `number` | no | Branch storage in GiB (gigabytes) |
| `instanceType` | body | `string` | no | New instance type for the branch |
| `backupConfiguration` | body | `object` | no | — |
| `hibernate` | body | `boolean` | no | Enabled when the branch should be hibernated, disabled if it needs to be reactivated. |
| `scaleToZero` | body | `object` | no | — |
| `postgresConfigurationParameters` | body | `object` | no | Arbitrary PostgreSQL configuration parameters for the cluster |
| `preloadLibraries[]` | body | `array` | no | List of PostgreSQL extensions and libraries to preload |
| `image` | body | `string` | no | PostgreSQL image to use for the database instances |
