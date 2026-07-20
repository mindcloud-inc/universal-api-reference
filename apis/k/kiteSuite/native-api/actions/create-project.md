# Create Project with KiteSuite

Creates a new project in KiteSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/project`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Create Project](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectName` | body | `string` | yes | Project name. |
| `projectType` | body | `string` | yes | Project type such as agile. |
| `projectLead` | body | `string` | yes | User ID of the project lead. |
| `avatar` | body | `string` | yes | Project avatar filename. |
| `description` | body | `string` | no | Project description. |
| `members[]` | body | `array<string>` | no | Email addresses to add to the project. Pass an array of emails. Send multiple values as a array. |
