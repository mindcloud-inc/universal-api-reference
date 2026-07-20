# Resolve a specific defect with Qase

Resolves a defect in Qase.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/defect/:code/resolve/:id`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Resolve a specific defect](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `id` | path | `number` | yes | Identifier. |
