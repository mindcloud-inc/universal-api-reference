# Update test suite with Qase

Updates an existing test suite in Qase.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/suite/:code/:id`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Update test suite](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `title` | body | `string` | no | Updated suite title. |
| `id` | path | `number` | yes | Identifier. |
