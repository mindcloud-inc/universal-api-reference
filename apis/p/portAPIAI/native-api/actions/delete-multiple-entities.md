# Delete Multiple Entities with Port API AI

Deletes multiple entities from Port.

## Endpoint

- **Method:** `POST`
- **Path:** `/blueprints/:blueprint_identifier/bulk/entities/delete`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Delete Multiple Entities](https://docs.port.io/api-reference/delete-multiple-entities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_identifier` | path | `string` | no | The Port blueprint identifier. |
| `entities[]` | body | `array<string>` | yes | Entity identifiers to delete |
