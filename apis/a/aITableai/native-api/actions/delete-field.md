# Delete Field with AITable.ai

Deletes an existing datasheet field from AITable.ai.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/fusion/v1/spaces/:spaceId/datasheets/:datasheetId/fields/:fieldId`
- **Base URL:** `https://aitable.ai`
- **Official documentation:** [Delete Field](https://developers.aitable.ai/api/reference/#delete-field)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | AITable space ID containing the datasheet. |
| `datasheetId` | path | `string` | yes | AITable datasheet ID containing the field. |
| `fieldId` | path | `string` | yes | AITable field ID to delete. |
