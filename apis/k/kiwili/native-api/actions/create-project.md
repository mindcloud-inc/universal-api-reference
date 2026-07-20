# Create Project with Kiwili

Creates a new project in Kiwili.

## Endpoint

- **Method:** `POST`
- **Path:** `/project`
- **Base URL:** `https://mindcloud.kiwili.com/api`
- **Official documentation:** [Create Project](https://api.kiwili.com/api/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Active` | body | `boolean` | no | Whether the project is active. |
| `EnterpriseId` | body | `number` | yes | The client enterprise ID for the project. |
| `Name` | body | `string` | yes | The project name. |
