# Get Project with MILKEE

Retrieves a project from MILKEE.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:companyId/projects/:projectId`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Get Project](https://apidocs.milkee.ch/api/resources/projects.html#einzelnes-project-abrufen)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
| `project` | path | `string` | yes | The numeric MILKEE project ID used in the request path. |
