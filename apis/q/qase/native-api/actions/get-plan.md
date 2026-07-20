# Get a specific plan with Qase

Retrieves a test plan from Qase.

## Endpoint

- **Method:** `GET`
- **Path:** `/plan/:code/:id`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Get a specific plan](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `id` | path | `number` | yes | Identifier. |
