# Assign Issue with Jira Software Cloud

Updates an issue assignee in Jira Software Cloud.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey/assignee`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Assign Issue](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issues/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | yes | Atlassian account ID to assign the issue to. |
| `cloudId` | path | `string` | yes | Jira cloud site ID returned by Accessible Resources. |
| `issueIdOrKey` | path | `string` | yes | Issue ID or key such as PROJ-123. |
