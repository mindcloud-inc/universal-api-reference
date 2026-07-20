# Get Task with Planfix

Retrieves a task from Planfix.

## Endpoint

- **Method:** `GET`
- **Path:** `/task/:id`
- **Base URL:** `{accountBaseUrl}/rest`
- **Official documentation:** [Get Task](https://help.planfix.com/restapidocs/#/Task/get-task-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Planfix task identifier. |
| `fields` | query | `string` | no | Comma-delimited task fields to return. |
