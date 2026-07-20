# Get Project Statuses with Jira Software Cloud

Retrieves project statuses from Jira Software Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/ex/jira/:cloudId/rest/api/3/project/:projectIdOrKey/statuses`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Get Project Statuses](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-projects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Jira cloud site ID returned by Accessible Resources. |
| `projectIdOrKey` | path | `string` | yes | Project ID or key such as ENG. |
