# Create a new test suite with Qase

Creates a new test suite in Qase.

## Endpoint

- **Method:** `POST`
- **Path:** `/suite/:code`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Create a new test suite](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `title` | body | `string` | yes | Test suite title. |
