# Update plan with Qase

Updates an existing test plan in Qase.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/plan/:code/:id`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Update plan](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `title` | body | `string` | no | Updated plan title. |
| `id` | path | `number` | yes | Identifier. |
