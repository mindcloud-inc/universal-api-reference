# Get a specific shared step with Qase

Retrieves a shared step from Qase.

## Endpoint

- **Method:** `GET`
- **Path:** `/shared_step/:code/:hash`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Get a specific shared step](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `hash` | path | `string` | yes | Hash. |
