# Update Cast with Anvil

Updates an existing cast in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Update Cast](https://www.useanvil.com/docs/api/graphql/reference/#mutation-updateCast)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.eid` | body | `string` | yes | Provide EID for Update Cast. |
| `variables.name` | body | `string` | no | Provide Name for Update Cast. |
| `variables.title` | body | `string` | no | Provide Title for Update Cast. |
| `variables.isTemplate` | body | `boolean` | no | Provide Is Template for Update Cast. |
| `variables.organizationEid` | body | `string` | no | Provide Organization EID for Update Cast. |
| `variables.config` | body | `object` | no | Provide Config for Update Cast. |
| `variables.configFile` | body | `file` | no | Provide Config File for Update Cast. |
| `variables.file` | body | `file` | no | Provide File for Update Cast. |
| `variables.isArchived` | body | `boolean` | no | Provide Is Archived for Update Cast. |
| `variables.versionNumber` | body | `number` | no | Provide Version Number for Update Cast. |
| `variables.allowedAliasIds[]` | body | `array<string>` | no | Provide Allowed Alias Ids for Update Cast. |
| `variables.feedbackRating` | body | `number` | no | Provide Feedback Rating for Update Cast. |
| `variables.feedbackMessage` | body | `string` | no | Provide Feedback Message for Update Cast. |
