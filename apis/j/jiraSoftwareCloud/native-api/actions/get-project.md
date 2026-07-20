# Get Project with Jira Software Cloud

Retrieves a project from Jira Software Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/ex/jira/:cloudId/rest/api/3/project/:projectIdOrKey`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Get Project](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-projects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Jira cloud site ID returned by Accessible Resources. |
| `projectIdOrKey` | path | `string` | yes | Project ID or key such as ENG. |
