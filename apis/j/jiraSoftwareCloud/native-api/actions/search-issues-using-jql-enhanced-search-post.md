# Search Issues Using JQL Enhanced Search (POST) with Jira Software Cloud

Finds issues in Jira Software Cloud using JQL.

## Endpoint

- **Method:** `POST`
- **Path:** `/ex/jira/:cloudId/rest/api/3/search/jql`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Search Issues Using JQL Enhanced Search (POST)](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issue-search/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Jira cloud site ID returned by Accessible Resources. |
| `jql` | body | `string` | yes | JQL query string. |
| `fields[]` | body | `array<string>` | no | Optional Jira issue fields to include in each search result. |
| `maxResults` | body | `number` | no | Optional maximum number of issues to return. |
| `nextPageToken` | body | `string` | no | Optional pagination token returned by Jira enhanced search. |
