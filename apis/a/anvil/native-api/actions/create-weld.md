# Create Weld with Anvil

Creates a new weld in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Create Weld](https://www.useanvil.com/docs/api/graphql/reference/#mutation-createWeld)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.organizationEid` | body | `string` | no | Provide Organization EID for Create Weld. |
| `variables.name` | body | `string` | no | Provide Name for Create Weld. |
| `variables.slug` | body | `string` | no | Provide Slug for Create Weld. |
| `variables.visibility` | body | `string` | no | Provide Visibility for Create Weld. |
| `variables.draftStep` | body | `string` | no | Provide Draft Step for Create Weld. |
| `variables.config` | body | `object` | no | Provide Config for Create Weld. |
| `variables.castEid` | body | `string` | no | Provide Cast EID for Create Weld. |
| `variables.files[]` | body | `array<object>` | no | Provide Files for Create Weld. |
| `variables.createCastTemplatesFromUploads` | body | `boolean` | no | Provide Create Cast Templates From Uploads for Create Weld. |
| `variables.advancedCreate` | body | `boolean` | no | Provide Advanced Create for Create Weld. |
| `variables.advancedDetectFields` | body | `boolean` | no | Provide Advanced Detect Fields for Create Weld. |
| `variables.detectBoxesAdvanced` | body | `boolean` | no | Provide Detect Boxes Advanced for Create Weld. |
