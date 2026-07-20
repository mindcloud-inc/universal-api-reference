# Update Comment with Jira Software Cloud

Updates an existing comment in Jira Software Cloud.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey/comment/:id`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Update Comment](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issue-comments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Updated Atlassian Document Format comment body payload. |
| `cloudId` | path | `string` | yes | Jira cloud site ID returned by Accessible Resources. |
| `id` | path | `string` | yes | Comment ID. |
| `issueIdOrKey` | path | `string` | yes | Issue ID or key such as PROJ-123. |
