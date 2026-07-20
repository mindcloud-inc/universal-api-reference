# Get Create Metadata Issue Types For Project with Jira Software Cloud

Retrieves project issue types for Jira Software Cloud issue creation.

## Endpoint

- **Method:** `GET`
- **Path:** `/ex/jira/:cloudId/rest/api/3/issue/createmeta/:projectIdOrKey/issuetypes`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Get Create Metadata Issue Types For Project](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issues/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Jira cloud site ID returned by Accessible Resources. |
| `projectIdOrKey` | path | `string` | yes | Project ID or key such as ENG. |
