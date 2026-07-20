# Create a new run with Qase

Creates a new test run in Qase.

## Endpoint

- **Method:** `POST`
- **Path:** `/run/:code`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Create a new run](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `title` | body | `string` | yes | Required request field title. |
