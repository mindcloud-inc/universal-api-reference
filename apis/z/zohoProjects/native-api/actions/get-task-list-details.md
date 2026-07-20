# Get Task List Details with Zoho Projects

Retrieves task list details from Zoho Projects.

## Endpoint

- **Method:** `GET`
- **Path:** `/portal/[:PORTALID]/projects/[:PROJECTID]/tasklists/[:TASKLISTID]`
- **Base URL:** `https://projectsapi.zoho.com/api/v3`
- **Official documentation:** [Get Task List Details](https://projectsapi.zoho.com/api-docs#task-lists_get-task-list-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PORTALID` | path | `string` | yes | Zoho Projects portal ID. |
| `PROJECTID` | path | `string` | yes | Zoho Projects project ID. |
| `TASKLISTID` | path | `string` | yes | Zoho Projects task list ID. |
