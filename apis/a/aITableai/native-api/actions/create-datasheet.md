# Create Datasheet with AITable.ai

Creates a new datasheet in AITable.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/fusion/v1/spaces/:spaceId/datasheets`
- **Base URL:** `https://aitable.ai`
- **Official documentation:** [Create Datasheet](https://developers.aitable.ai/api/reference/#create-datasheet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional datasheet description. Maximum 500 characters. |
| `spaceId` | path | `string` | yes | AITable space ID where the datasheet will be created. |
| `name` | body | `string` | yes | Name of the datasheet to create. Maximum 100 characters. |
| `folderId` | body | `string` | no | Optional folder node ID. If omitted, AITable creates the datasheet in the working directory. |
| `fields[]` | body | `array<object>` | no | Optional array of field definitions to create with the datasheet. AITable allows up to 200 fields. |
