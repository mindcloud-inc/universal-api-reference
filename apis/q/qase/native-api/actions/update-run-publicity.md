# Update publicity of a specific run with Qase

Updates test run publicity in Qase.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/run/:code/:id/public`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Update publicity of a specific run](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `id` | path | `number` | yes | Identifier. |
| `status` | body | `boolean` | yes | Required request field status. |
