# List Workflow Activity with MindCloud

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/workflow-activity`
- **Base URL:** `https://connect.mindcloud.co`
- **Official documentation:** [List Workflow Activity](https://mindcloud.co/docs/api/rest/actions/list-workflow-activity)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowId` | query | `list<string>` | no | Only rows of this workflow. |
| `from` | query | `string` | no | First day of the window, as YYYY-MM-DD (UTC). Defaults to 29 days before To. |
| `to` | query | `string` | no | Last day of the window, as YYYY-MM-DD (UTC), included. Defaults to today. A window covers at most 92 days. |
