# Update Records with AITable.ai

Updates existing records in a datasheet in AITable.ai.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/fusion/v1/datasheets/:datasheetId/records`
- **Base URL:** `https://aitable.ai`
- **Official documentation:** [Update Records](https://developers.aitable.ai/api/reference/#update-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasheetId` | path | `string` | yes | AITable datasheet ID where records will be updated. |
| `records[]` | body | `array<object>` | yes | Array of records to update. Each item contains recordId and fields. |
| `fieldKey` | body | `string` | no | Use field names or field IDs when writing fields. AITable supports name or id. |
