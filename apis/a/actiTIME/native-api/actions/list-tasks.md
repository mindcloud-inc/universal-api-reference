# List Tasks with actiTIME

Retrieves a list of tasks from actiTIME.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [List Tasks](https://www.actitime.com/api-documentation/tasks-resource)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerIds` | query | `string` | no | Comma-separated customer ids to retrieve tasks from. |
| `ids` | query | `string` | no | Comma-separated ids of tasks to be returned. |
| `includeReferenced` | query | `string` | no | Comma-separated referenced objects to include. |
| `name` | query | `string` | no | Exact task name match, case-insensitive. |
| `projectIds` | query | `string` | no | Comma-separated project ids to retrieve tasks from. |
| `sort` | query | `string` | no | Sorting tokens like +name or -status. |
| `status` | query | `string` | no | Task status filter such as open or completed. |
| `typeOfWorkIds` | query | `string` | no | Comma-separated type of work ids associated with tasks to be returned. |
| `words` | query | `string` | no | Return tasks containing all given words in the name. |
| `workflowStatusIds` | query | `string` | no | Comma-separated workflow status ids associated with tasks to be returned. |
