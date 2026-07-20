# Delete Task List with Zoho Projects

Deletes an existing task list from Zoho Projects.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/portal/[:PORTALID]/projects/[:PROJECTID]/tasklists/[:TASKLISTID]`
- **Base URL:** `https://projectsapi.zoho.com/api/v3`
- **Official documentation:** [Delete Task List](https://projectsapi.zoho.com/api-docs#task-lists_delete-task-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PORTALID` | path | `string` | yes | Portal identifier from Zoho Projects. |
| `PROJECTID` | path | `string` | yes | Project identifier from Zoho Projects. |
| `TASKLISTID` | path | `string` | yes | Task list identifier from Zoho Projects. |
