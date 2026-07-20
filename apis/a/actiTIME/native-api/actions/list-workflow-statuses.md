# List Workflow Statuses with actiTIME

Retrieves a list of workflow statuses from actiTIME.

## Endpoint

- **Method:** `GET`
- **Path:** `/workflowStatuses`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [List Workflow Statuses](https://www.actitime.com/api-documentation/workflow-statuses-resource)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | no | Comma-separated workflow status ids to be returned. |
| `name` | query | `string` | no | Exact workflow status name match, case-insensitive. |
| `sort` | query | `string` | no | Sorting tokens like +name or -type. |
| `type` | query | `string` | no | Workflow status group such as open or completed. |
| `words` | query | `string` | no | Return workflow statuses containing all given words in the name. |
