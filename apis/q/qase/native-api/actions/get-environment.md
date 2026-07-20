# Get a specific environment with Qase

Retrieves an environment from Qase.

## Endpoint

- **Method:** `GET`
- **Path:** `/environment/:code/:id`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Get a specific environment](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `id` | path | `number` | yes | Identifier. |
