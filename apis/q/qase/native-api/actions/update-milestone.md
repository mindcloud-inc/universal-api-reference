# Update milestone with Qase

Updates an existing milestone in Qase.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/milestone/:code/:id`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Update milestone](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `title` | body | `string` | no | Updated milestone title. |
| `id` | path | `number` | yes | Identifier. |
