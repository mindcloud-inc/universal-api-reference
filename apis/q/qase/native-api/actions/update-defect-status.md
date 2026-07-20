# Update a specific defect status with Qase

Updates a defect status in Qase.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/defect/:code/status/:id`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Update a specific defect status](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `id` | path | `number` | yes | Identifier. |
| `status` | body | `string` | yes | Required request field status. |
