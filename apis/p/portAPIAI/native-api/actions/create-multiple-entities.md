# Create Multiple Entities with Port API AI

Creates multiple entities in Port.

## Endpoint

- **Method:** `POST`
- **Path:** `/blueprints/:blueprint_identifier/entities/bulk`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Create Multiple Entities](https://docs.port.io/api-reference/create-multiple-entities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_identifier` | path | `string` | no | The Port blueprint identifier. |
| `entities[]` | body | `array<object>` | yes | Entities to create |
