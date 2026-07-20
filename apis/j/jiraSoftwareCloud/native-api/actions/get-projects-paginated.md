# Get Projects Paginated with Jira Software Cloud

Retrieves projects from Jira Software Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/ex/jira/:cloudId/rest/api/3/project/search`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Get Projects Paginated](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-projects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Jira cloud site ID returned by Accessible Resources. |
