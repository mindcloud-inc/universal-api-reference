# Get Project with Planfix

Retrieves a project from Planfix.

## Endpoint

- **Method:** `GET`
- **Path:** `/project/:id`
- **Base URL:** `{accountBaseUrl}/rest`
- **Official documentation:** [Get Project](https://help.planfix.com/restapidocs/#/Project/get-project-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Planfix project identifier. |
| `fields` | query | `string` | no | Comma-delimited project fields to return. |
