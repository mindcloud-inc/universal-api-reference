# Update shared step with Qase

Updates an existing shared step in Qase.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/shared_step/:code/:hash`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Update shared step](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `hash` | path | `string` | yes | Hash. |
| `title` | body | `string` | yes | Required request field title. |
