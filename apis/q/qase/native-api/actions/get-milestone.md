# Get a specific milestone with Qase

Retrieves a milestone from Qase.

## Endpoint

- **Method:** `GET`
- **Path:** `/milestone/:code/:id`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Get a specific milestone](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `id` | path | `number` | yes | Identifier. |
