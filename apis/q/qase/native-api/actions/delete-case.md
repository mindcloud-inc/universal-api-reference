# Delete test case with Qase

Deletes a test case from Qase.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/case/:code/:id`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Delete test case](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `id` | path | `number` | yes | Identifier. |
