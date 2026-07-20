# Search Entities with Port API AI

Finds entities in Port.

## Endpoint

- **Method:** `POST`
- **Path:** `/entities/search`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Search Entities](https://docs.port.io/api-reference/search-entities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `combinator` | body | `string` | yes | Search combinator |
| `rules[]` | body | `array<object>` | yes | Search rules |
