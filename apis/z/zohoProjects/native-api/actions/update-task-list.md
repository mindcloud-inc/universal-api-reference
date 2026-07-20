# Update Task List with Zoho Projects

Updates an existing task list in Zoho Projects.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/portal/[:PORTALID]/projects/[:PROJECTID]/tasklists/[:TASKLISTID]`
- **Base URL:** `https://projectsapi.zoho.com/api/v3`
- **Official documentation:** [Update Task List](https://projectsapi.zoho.com/api-docs#task-lists_update-task-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PORTALID` | path | `string` | yes | Portal identifier from Zoho Projects. |
| `PROJECTID` | path | `string` | yes | Project identifier from Zoho Projects. |
| `TASKLISTID` | path | `string` | yes | Task list identifier from Zoho Projects. |
| `name` | body | `string` | no | Task list name. |
| `milestone.id` | body | `string` | no | Associated milestone identifier. |
| `flag` | body | `string` | no | Task list flag. Accepted values: internal, external. |
| `status` | body | `string` | no | Task list status. |
