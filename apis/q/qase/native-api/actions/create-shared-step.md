# Create a new shared step with Qase

Creates a new shared step in Qase.

## Endpoint

- **Method:** `POST`
- **Path:** `/shared_step/:code`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Create a new shared step](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `title` | body | `string` | yes | Required request field title. |
