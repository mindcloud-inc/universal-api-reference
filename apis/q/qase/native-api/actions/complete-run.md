# Complete a specific run with Qase

Completes a test run in Qase.

## Endpoint

- **Method:** `POST`
- **Path:** `/run/:code/:id/complete`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Complete a specific run](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `id` | path | `number` | yes | Identifier. |
