# Create Task with Planfix

Creates a new task in Planfix.

## Endpoint

- **Method:** `POST`
- **Path:** `/task/`
- **Base URL:** `{accountBaseUrl}/rest`
- **Official documentation:** [Create Task](https://help.planfix.com/restapidocs/#/Task/post-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Task name. |
| `description` | body | `string` | no | Task description. |
