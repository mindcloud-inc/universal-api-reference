# Delete run with Qase

Deletes a test run from Qase.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/run/:code/:id`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Delete run](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `id` | path | `number` | yes | Identifier. |
