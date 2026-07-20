# Get Task Details with Zoho Projects

Retrieves task details from Zoho Projects.

## Endpoint

- **Method:** `GET`
- **Path:** `/portal/[:PORTALID]/projects/[:PROJECTID]/tasks/[:TASKID]`
- **Base URL:** `https://projectsapi.zoho.com/api/v3`
- **Official documentation:** [Get Task Details](https://projectsapi.zoho.com/api-docs#tasks_get-task-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PORTALID` | path | `string` | yes | Zoho Projects portal ID. |
| `PROJECTID` | path | `string` | yes | Zoho Projects project ID. |
| `TASKID` | path | `string` | yes | Zoho Projects task ID. |
