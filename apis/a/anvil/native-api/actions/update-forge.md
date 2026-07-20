# Update Forge with Anvil

Updates an existing forge in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Update Forge](https://www.useanvil.com/docs/api/graphql/reference/#mutation-updateForge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.eid` | body | `string` | yes | Provide EID for Update Forge. |
| `variables.name` | body | `string` | no | Provide Name for Update Forge. |
| `variables.slug` | body | `string` | no | Provide Slug for Update Forge. |
| `variables.config` | body | `object` | no | Provide Config for Update Forge. |
| `variables.configFile` | body | `file` | no | Provide Config File for Update Forge. |
| `variables.isArchived` | body | `boolean` | no | Provide Is Archived for Update Forge. |
| `variables.isRequired` | body | `boolean` | no | Provide Is Required for Update Forge. |
| `variables.title` | body | `string` | no | Provide Title for Update Forge. |
| `variables.organizationRole` | body | `string` | no | Provide Organization Role for Update Forge. |
| `variables.unauthenticatedAuthType` | body | `string` | no | Provide Unauthenticated Auth Type for Update Forge. |
| `variables.versionNumber` | body | `number` | no | Provide Version Number for Update Forge. |
