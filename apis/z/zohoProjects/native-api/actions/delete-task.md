# Delete Task with Zoho Projects

Deletes an existing task from Zoho Projects.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/portal/[:PORTALID]/projects/[:PROJECTID]/tasks/[:TASKID]`
- **Base URL:** `https://projectsapi.zoho.com/api/v3`
- **Official documentation:** [Delete Task](https://projectsapi.zoho.com/api-docs#tasks_delete-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PORTALID` | path | `string` | yes | Zoho Projects portal ID. |
| `PROJECTID` | path | `string` | yes | Zoho Projects project ID. |
| `TASKID` | path | `string` | yes | Zoho Projects task ID. |
