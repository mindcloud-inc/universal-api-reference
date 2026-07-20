# Create Records with AITable.ai

Creates new records in a datasheet in AITable.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/fusion/v1/datasheets/:datasheetId/records`
- **Base URL:** `https://aitable.ai`
- **Official documentation:** [Create Records](https://developers.aitable.ai/api/reference/#create-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasheetId` | path | `string` | yes | AITable datasheet ID where records will be created. |
| `records[]` | body | `array<object>` | yes | Array of records to create. Each item contains a fields object. |
| `fieldKey` | body | `string` | no | Use field names or field IDs when writing fields. AITable supports name or id. |
