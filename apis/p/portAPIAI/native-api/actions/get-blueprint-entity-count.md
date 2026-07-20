# Get Blueprint Entity Count with Port API AI

Retrieves a blueprint's entity count from Port.

## Endpoint

- **Method:** `GET`
- **Path:** `/blueprints/:blueprint_identifier/entities-count`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Get Blueprint Entity Count](https://docs.port.io/api-reference/get-a-blueprints-entity-count)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_identifier` | path | `string` | yes | The blueprint identifier. |
