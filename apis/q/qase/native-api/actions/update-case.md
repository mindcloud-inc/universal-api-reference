# Update test case with Qase

Updates an existing test case in Qase.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/case/:code/:id`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Update test case](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `title` | body | `string` | no | Updated case title. |
| `id` | path | `number` | yes | Identifier. |
