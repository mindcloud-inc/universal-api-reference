# Create Project with zipBoard

Creates a new project in zipBoard.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://app.zipboard.co/api/v1`
- **Official documentation:** [Create Project](https://help.zipboard.co/article/178-api-for-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Project description. |
| `orgid` | body | `string` | no | Optional organization ID where the project should be created. |
| `projectid` | body | `string` | no | Optional custom project ID. |
| `title` | body | `string` | yes | Project title. |
