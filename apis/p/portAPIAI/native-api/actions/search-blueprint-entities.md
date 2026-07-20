# Search Blueprint Entities with Port API AI

Finds entities in a Port blueprint.

## Endpoint

- **Method:** `POST`
- **Path:** `/blueprints/:blueprint_identifier/entities/search`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Search Blueprint Entities](https://docs.port.io/api-reference/search-a-blueprints-entities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_identifier` | path | `string` | yes | The Port blueprint identifier. |
| `query` | body | `object` | yes | Blueprint entity query |
