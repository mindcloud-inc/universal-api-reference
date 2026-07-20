# Create a Project with Beebole

Creates a new project in Beebole.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://beebole-apps.com/api/v2`
- **Official documentation:** [Create a Project](https://beebole.com/help/api#create-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project.name` | body | `string` | yes | Name for the project to create. |
| `project.startDate` | body | `string` | no | Project start date in YYYY-MM-DD format. |
| `project.description` | body | `string` | no | Project description. |
| `project.company.id` | body | `number` | yes | The Beebole company ID that owns the project. |
