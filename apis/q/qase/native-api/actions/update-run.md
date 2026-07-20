# Update a specific run with Qase

Updates an existing test run in Qase.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/run/:code/:id`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Update a specific run](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `title` | body | `string` | no | Updated run title. |
| `id` | path | `number` | yes | Identifier. |
