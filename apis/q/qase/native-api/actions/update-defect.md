# Update defect with Qase

Updates an existing defect in Qase.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/defect/:code/:id`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Update defect](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `title` | body | `string` | no | Updated defect title. |
| `id` | path | `number` | yes | Identifier. |
