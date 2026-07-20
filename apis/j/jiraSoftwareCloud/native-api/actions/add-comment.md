# Add Comment with Jira Software Cloud

Creates a new comment in Jira Software Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey/comment`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Add Comment](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issue-comments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Atlassian Document Format comment body payload. |
| `cloudId` | path | `string` | yes | Jira cloud site ID returned by Accessible Resources. |
| `issueIdOrKey` | path | `string` | yes | Issue ID or key such as PROJ-123. |
