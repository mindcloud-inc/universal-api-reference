# Rename Blueprint Property with Port API AI

Updates a blueprint property name in Port.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/blueprints/:blueprint_identifier/properties/:property_identifier/rename`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Rename Blueprint Property](https://docs.port.io/api-reference/rename-a-property-in-a-blueprint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_identifier` | path | `string` | yes | The blueprint identifier. |
| `identifier` | body | `string` | no | New identifier for the property. |
| `property_identifier` | path | `string` | yes | The property identifier. |
