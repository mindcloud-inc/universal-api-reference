# Create Project with GoodDay.work

Creates a new project in GoodDay.work.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/new-project`
- **Base URL:** `https://api.goodday.work/2.0`
- **Official documentation:** [Create Project](https://www.goodday.work/developers/api-v2/projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `createdByUserId` | body | `string` | yes | ID of user on whose behalf project is created. |
| `projectTemplateId` | body | `string` | yes | Project template ID. |
| `name` | body | `string` | yes | Project name. |
