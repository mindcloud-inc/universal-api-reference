# Delete test run result with Qase

Deletes a test run result from Qase.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/result/:code/:id/:hash`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Delete test run result](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `id` | path | `number` | yes | Identifier. |
| `hash` | path | `string` | yes | Hash. |
