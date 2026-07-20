# Update Team with Port API AI

Updates a team in Port.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/teams/:name`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Update Team](https://docs.port.io/api-reference/update-a-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The Port team name. |
| `description` | body | `string` | no | The updated team description. |
