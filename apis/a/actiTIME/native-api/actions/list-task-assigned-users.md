# List Task Assigned Users with actiTIME

Retrieves users assigned to a task in actiTIME.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/:id/assignedUsers`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [List Task Assigned Users](https://www.actitime.com/api-documentation/tasks-resource)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Task identifier. |
