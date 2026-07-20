# Get test run result by code with Qase

Retrieves a test run result from Qase by hash.

## Endpoint

- **Method:** `GET`
- **Path:** `/result/:code/:hash`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Get test run result by code](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `hash` | path | `string` | yes | Hash. |
