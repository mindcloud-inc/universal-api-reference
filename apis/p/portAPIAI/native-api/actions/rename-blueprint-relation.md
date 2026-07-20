# Rename Blueprint Relation with Port API AI

Updates a blueprint relation name in Port.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/blueprints/:blueprint_identifier/relations/:relation_identifier/rename`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Rename Blueprint Relation](https://docs.port.io/api-reference/rename-a-blueprints-relation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_identifier` | path | `string` | yes | The blueprint identifier. |
| `identifier` | body | `string` | no | New identifier for the relation. |
| `relation_identifier` | path | `string` | yes | The relation identifier. |
