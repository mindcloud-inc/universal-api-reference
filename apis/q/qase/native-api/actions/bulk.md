# Create test cases in bulk with Qase

Creates multiple test cases in Qase.

## Endpoint

- **Method:** `POST`
- **Path:** `/case/:code/bulk`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Create test cases in bulk](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `cases[]` | body | `array<string>` | yes | Required request field cases. |
