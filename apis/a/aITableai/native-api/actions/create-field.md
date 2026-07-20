# Create Field with AITable.ai

Creates a new datasheet field in AITable.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/fusion/v1/spaces/:spaceId/datasheets/:datasheetId/fields`
- **Base URL:** `https://aitable.ai`
- **Official documentation:** [Create Field](https://developers.aitable.ai/api/reference/#create-field)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | AITable space ID containing the datasheet. |
| `datasheetId` | path | `string` | yes | AITable datasheet ID where the field will be created. |
| `name` | body | `string` | yes | Name of the field to create. |
| `type` | body | `string` | yes | AITable field type, for example Text, SingleText, Number, DateTime, or SingleSelect. |
