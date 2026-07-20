# Search Issues Using JQL Enhanced Search (GET) with Jira Software Cloud

Finds issues in Jira Software Cloud using JQL.

## Endpoint

- **Method:** `GET`
- **Path:** `/ex/jira/:cloudId/rest/api/3/search/jql`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Search Issues Using JQL Enhanced Search (GET)](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issue-search/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Jira cloud site ID returned by Accessible Resources. |
| `jql` | query | `string` | yes | JQL query string. |
