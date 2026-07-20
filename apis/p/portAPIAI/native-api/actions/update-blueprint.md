# Update Blueprint with Port API AI

Updates a blueprint in Port.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/blueprints/:identifier`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Update Blueprint](https://docs.port.io/api-reference/update-a-blueprint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `icon` | body | `string` | no | Blueprint icon |
| `identifier` | path | `string` | yes | The Port blueprint identifier. |
| `title` | body | `string` | no | Blueprint title |
