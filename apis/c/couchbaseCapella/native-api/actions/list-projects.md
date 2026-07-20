# List Projects with Couchbase Capella

Retrieves projects from Couchbase Capella.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/organizations/:organizationId/projects`
- **Base URL:** `https://cloudapi.cloud.couchbase.com`
- **Official documentation:** [List Projects](https://docs.couchbase.com/cloud/management-api-reference/index.html#tag/Projects/operation/listProjects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | The GUID4 ID of the organization. |
