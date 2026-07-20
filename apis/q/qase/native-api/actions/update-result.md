# Update test run result with Qase

Updates an existing test run result in Qase.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/result/:code/:id/:hash`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Update test run result](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `status` | body | `string` | no | Updated result status. |
| `id` | path | `number` | yes | Identifier. |
| `hash` | path | `string` | yes | Hash. |
