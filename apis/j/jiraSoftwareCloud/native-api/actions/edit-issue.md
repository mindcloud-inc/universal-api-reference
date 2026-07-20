# Edit Issue with Jira Software Cloud

Updates an existing issue in Jira Software Cloud.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Edit Issue](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issues/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Jira cloud site ID returned by Accessible Resources. |
| `fields` | body | `object` | no | Issue fields object to update. |
| `issueIdOrKey` | path | `string` | yes | Issue ID or key such as PROJ-123. |
| `returnIssue` | query | `boolean` | no | When true, Jira returns the updated issue in the response. |
