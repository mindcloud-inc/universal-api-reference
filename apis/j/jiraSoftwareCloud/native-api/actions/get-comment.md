# Get Comment with Jira Software Cloud

Retrieves a comment from Jira Software Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey/comment/:id`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Get Comment](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issue-comments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Jira cloud site ID returned by Accessible Resources. |
| `id` | path | `string` | yes | Comment ID. |
| `issueIdOrKey` | path | `string` | yes | Issue ID or key such as PROJ-123. |
