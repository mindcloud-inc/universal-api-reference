# Create test run result with Qase

Creates a test run result in Qase.

## Endpoint

- **Method:** `POST`
- **Path:** `/result/:code/:id`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Create test run result](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `id` | path | `number` | yes | Identifier. |
| `status` | body | `string` | yes | Can have the following values `passed`, `failed`, `blocked`, `skipped`, `invalid` + custom statuses |
