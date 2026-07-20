# Bulk create test run result with Qase

Creates multiple test run results in Qase.

## Endpoint

- **Method:** `POST`
- **Path:** `/result/:code/:id/bulk`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Bulk create test run result](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `id` | path | `number` | yes | Identifier. |
| `results[]` | body | `array<string>` | yes | Required request field results. |
