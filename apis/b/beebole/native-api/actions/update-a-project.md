# Update a Project with Beebole

Updates an existing project in Beebole.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://beebole-apps.com/api/v2`
- **Official documentation:** [Update a Project](https://beebole.com/help/api#update-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project.id` | body | `number` | yes | The Beebole project ID to update. |
| `project.name` | body | `string` | no | Updated project name. |
| `project.startDate` | body | `string` | no | Updated project start date in YYYY-MM-DD format. |
| `project.description` | body | `string` | no | Updated project description. |
