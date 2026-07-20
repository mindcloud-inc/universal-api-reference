# Update shared parameter with Qase

Updates an existing shared parameter in Qase.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/shared_parameter/:id`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Update shared parameter](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Identifier. |
| `title` | body | `string` | no | Updated shared parameter title. |
