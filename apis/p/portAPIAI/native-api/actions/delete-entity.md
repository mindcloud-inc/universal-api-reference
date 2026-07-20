# Delete Entity with Port API AI

Deletes an entity from Port.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/blueprints/:blueprint_identifier/entities/:entity_identifier`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Delete Entity](https://docs.port.io/api-reference/delete-an-entity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_identifier` | path | `string` | no | The Port blueprint identifier. |
| `entity_identifier` | path | `string` | no | The Port entity identifier. |
