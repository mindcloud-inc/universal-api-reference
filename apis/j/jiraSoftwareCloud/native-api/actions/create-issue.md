# Create Issue with Jira Software Cloud

Creates a new issue in Jira Software Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/ex/jira/:cloudId/rest/api/3/issue`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Create Issue](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issues/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Jira cloud site ID returned by Accessible Resources. |
| `fields` | body | `object` | yes | Issue fields object for the new issue. |
