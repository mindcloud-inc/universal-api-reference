# Create Cast with Anvil

Creates a new cast in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Create Cast](https://www.useanvil.com/docs/api/graphql/reference/#mutation-createCast)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.organizationEid` | body | `string` | no | Provide Organization EID for Create Cast. |
| `variables.title` | body | `string` | no | Provide Title for Create Cast. |
| `variables.file` | body | `file` | yes | Provide File for Create Cast. |
| `variables.isTemplate` | body | `boolean` | no | Provide Is Template for Create Cast. |
| `variables.allowedAliasIds[]` | body | `array<string>` | no | Provide Allowed Alias Ids for Create Cast. |
| `variables.detectFields` | body | `boolean` | no | Provide Detect Fields for Create Cast. |
| `variables.advancedDetectFields` | body | `boolean` | no | Provide Advanced Detect Fields for Create Cast. |
| `variables.detectBoxesAdvanced` | body | `boolean` | no | Provide Detect Boxes Advanced for Create Cast. |
| `variables.aliasIds` | body | `object` | no | Provide Alias Ids for Create Cast. |
