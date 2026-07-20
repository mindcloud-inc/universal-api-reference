# Create Team with Port API AI

Creates a team in Port.

## Endpoint

- **Method:** `POST`
- **Path:** `/teams`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Create Team](https://docs.port.io/api-reference/create-a-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The Port team name. |
| `description` | body | `string` | no | The team description. |
