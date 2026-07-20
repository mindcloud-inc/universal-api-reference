# List Project Assigned Users with actiTIME

Retrieves users assigned to a project in actiTIME.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:id/assignedUsers`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [List Project Assigned Users](https://www.actitime.com/api-documentation/projects-resource)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Project identifier. |
