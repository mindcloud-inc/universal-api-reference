# Rename Blueprint Mirror Property with Port API AI

Updates a blueprint mirror property name in Port.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/blueprints/:blueprint_identifier/mirror/:property_identifier/rename`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Rename Blueprint Mirror Property](https://docs.port.io/api-reference/rename-a-blueprints-mirror-property)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_identifier` | path | `string` | yes | The blueprint identifier. |
| `identifier` | body | `string` | no | New identifier for the mirror property. |
| `property_identifier` | path | `string` | yes | The property identifier. |
