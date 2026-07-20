# Create a new environment with Qase

Creates a new environment in Qase.

## Endpoint

- **Method:** `POST`
- **Path:** `/environment/:code`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Create a new environment](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `title` | body | `string` | yes | Required request field title. |
| `slug` | body | `string` | yes | Required request field slug. |
