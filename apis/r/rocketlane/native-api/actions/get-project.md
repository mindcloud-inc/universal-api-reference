# Get Project with Rocketlane

Retrieves a project from Rocketlane.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.0/projects/:projectId`
- **Base URL:** `https://api.rocketlane.com/api`
- **Official documentation:** [Get Project](https://developer.rocketlane.com/reference/get-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | The project's unique, system-generated identifier, which can be used to identify the project globally. |
| `includeFields` | query | `list<string>` | no | This query parameter allows you to specify which fields should be returned in the response body by selecting from the drop down. To get the relevant fields, use comma separated values. If the field is left blank, the default properties are returned. |
| `includeAllFields` | query | `boolean` | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |
