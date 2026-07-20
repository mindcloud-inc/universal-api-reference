# Create a new test case with Qase

Creates a new test case in Qase.

## Endpoint

- **Method:** `POST`
- **Path:** `/case/:code`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Create a new test case](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `title` | body | `string` | yes | Required request field title. |
