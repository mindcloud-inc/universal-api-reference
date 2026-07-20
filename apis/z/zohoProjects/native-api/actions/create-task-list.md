# Create Task List with Zoho Projects

Creates a new task list in Zoho Projects.

## Endpoint

- **Method:** `POST`
- **Path:** `/portal/[:PORTALID]/projects/[:PROJECTID]/tasklists`
- **Base URL:** `https://projectsapi.zoho.com/api/v3`
- **Official documentation:** [Create Task List](https://projectsapi.zoho.com/api-docs#task-lists_create-task-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PORTALID` | path | `string` | yes | Portal identifier from Zoho Projects. |
| `PROJECTID` | path | `string` | yes | Project identifier from Zoho Projects. |
| `name` | body | `string` | yes | Task list name. |
| `milestone.id` | body | `string` | no | Associated milestone identifier. |
| `flag` | body | `string` | no | Task list flag. Accepted values: internal, external. |
| `status` | body | `string` | no | Task list status. |
