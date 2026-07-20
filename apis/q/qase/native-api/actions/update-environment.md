# Update environment with Qase

Updates an existing environment in Qase.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/environment/:code/:id`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Update environment](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `title` | body | `string` | no | Updated environment title. |
| `id` | path | `number` | yes | Identifier. |
