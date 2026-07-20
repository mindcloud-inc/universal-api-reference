# Delete test suite with Qase

Deletes a test suite from Qase.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/suite/:code/:id`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Delete test suite](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `id` | path | `number` | yes | Identifier. |
