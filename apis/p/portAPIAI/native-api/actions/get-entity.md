# Get Entity with Port API AI

Retrieves an entity from Port.

## Endpoint

- **Method:** `GET`
- **Path:** `/blueprints/:blueprint_identifier/entities/:entity_identifier`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Get Entity](https://docs.port.io/api-reference/get-an-entity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_identifier` | path | `string` | no | The Port blueprint identifier. |
| `entity_identifier` | path | `string` | no | The Port entity identifier. |
