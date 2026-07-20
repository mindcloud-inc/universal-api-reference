# Create Forge with Anvil

Creates a new forge in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Create Forge](https://www.useanvil.com/docs/api/graphql/reference/#mutation-createForge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.weldEid` | body | `string` | yes | Provide Weld EID for Create Forge. |
| `variables.name` | body | `string` | yes | Provide Name for Create Forge. |
| `variables.slug` | body | `string` | yes | Provide Slug for Create Forge. |
| `variables.config` | body | `object` | no | Provide Config for Create Forge. |
| `variables.castEid` | body | `string` | no | Provide Cast EID for Create Forge. |
| `variables.castFieldIds` | body | `object` | no | Provide Cast Field Ids for Create Forge. |
