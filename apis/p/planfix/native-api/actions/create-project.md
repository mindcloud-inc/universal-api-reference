# Create Project with Planfix

Creates a new project in Planfix.

## Endpoint

- **Method:** `POST`
- **Path:** `/project/`
- **Base URL:** `{accountBaseUrl}/rest`
- **Official documentation:** [Create Project](https://help.planfix.com/restapidocs/#/Project/post-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Project name. |
| `description` | body | `string` | no | Project description. |
