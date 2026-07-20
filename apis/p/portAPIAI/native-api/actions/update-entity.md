# Update Entity with Port API AI

Updates an entity in Port.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/blueprints/:blueprint_identifier/entities/:entity_identifier`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Update Entity](https://docs.port.io/api-reference/update-an-entity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_identifier` | path | `string` | yes | The Port blueprint identifier. |
| `entity_identifier` | path | `string` | yes | The Port entity identifier. |
| `title` | body | `string` | yes | Entity title |
