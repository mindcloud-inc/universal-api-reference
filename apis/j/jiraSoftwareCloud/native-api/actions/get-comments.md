# Get Comments with Jira Software Cloud

Retrieves issue comments from Jira Software Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey/comment`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Get Comments](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issue-comments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Jira cloud site ID returned by Accessible Resources. |
| `issueIdOrKey` | path | `string` | yes | Issue ID or key such as PROJ-123. |
