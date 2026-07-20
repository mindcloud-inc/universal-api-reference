# Get Current User with Jira Software Cloud

Retrieves the current Jira Software Cloud user.

## Endpoint

- **Method:** `GET`
- **Path:** `/ex/jira/:cloudId/rest/api/3/myself`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Get Current User](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-myself/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Jira cloud site ID returned by Accessible Resources. |
