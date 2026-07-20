# Transition Issue with Jira Software Cloud

Transitions an issue in Jira Software Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey/transitions`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Transition Issue](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issues/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Jira cloud site ID returned by Accessible Resources. |
| `issueIdOrKey` | path | `string` | yes | Issue ID or key such as PROJ-123. |
| `transition` | body | `object` | yes | Transition object containing the transition ID and optional field updates. |
