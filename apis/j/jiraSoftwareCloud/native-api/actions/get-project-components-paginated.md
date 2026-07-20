# Get Project Components Paginated with Jira Software Cloud

Retrieves project components from Jira Software Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/ex/jira/:cloudId/rest/api/3/project/:projectIdOrKey/component`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Get Project Components Paginated](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-project-components/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Jira cloud site ID returned by Accessible Resources. |
| `projectIdOrKey` | path | `string` | yes | Project ID or key such as ENG. |
