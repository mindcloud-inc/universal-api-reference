# Create Entity with Port API AI

Creates an entity in Port.

## Endpoint

- **Method:** `POST`
- **Path:** `/blueprints/:blueprint_identifier/entities`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Create Entity](https://docs.port.io/api-reference/create-an-entity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_identifier` | path | `string` | yes | The Port blueprint identifier. |
| `identifier` | body | `string` | yes | Entity identifier |
| `title` | body | `string` | yes | Entity title |
