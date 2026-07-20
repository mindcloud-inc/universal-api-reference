# Update Project with Time Doctor

Updates an existing project in Time Doctor.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/1.0/projects/:projectId`
- **Base URL:** `https://api2.timedoctor.com`
- **Official documentation:** [Update Project](https://api2.timedoctor.com/#operation/putProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | ID of the project to update. |
| `name` | body | `string` | no | Project name. |
| `description` | body | `string` | no | Project description. |
