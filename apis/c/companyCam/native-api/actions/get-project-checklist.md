# Get Project Checklist with CompanyCam

Retrieves a project checklist from CompanyCam.

## Endpoint

- **Method:** `GET`
- **Path:** `projects/:projectId/checklists/:checklistId`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [Get Project Checklist](https://docs.companycam.com/reference/getprojectchecklist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | — |
| `checklistId` | path | `string` | yes | The `id` of the Checklist you want to retrieve from the above Project. |
