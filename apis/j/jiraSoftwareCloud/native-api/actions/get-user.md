# Get User with Jira Software Cloud

Retrieves a user from Jira Software Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/ex/jira/:cloudId/rest/api/3/user`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Get User](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-users/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | yes | Atlassian account ID to fetch. |
| `cloudId` | path | `string` | yes | Jira cloud site ID returned by Accessible Resources. |
