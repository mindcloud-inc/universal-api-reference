# Delete defect with Qase

Deletes a defect from Qase.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/defect/:code/:id`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Delete defect](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `id` | path | `number` | yes | Identifier. |
