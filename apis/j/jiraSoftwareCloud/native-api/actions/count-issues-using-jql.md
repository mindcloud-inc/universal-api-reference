# Count Issues Using JQL with Jira Software Cloud

Retrieves an approximate JQL issue count from Jira Software Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/ex/jira/:cloudId/rest/api/3/search/approximate-count`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Count Issues Using JQL](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issue-search/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Jira cloud site ID returned by Accessible Resources. |
| `jql` | body | `string` | yes | JQL query string to count. |
