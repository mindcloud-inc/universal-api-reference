# List Fields with AITable.ai

Retrieves fields from a datasheet in AITable.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/fusion/v1/datasheets/:datasheetId/fields`
- **Base URL:** `https://aitable.ai`
- **Official documentation:** [List Fields](https://developers.aitable.ai/api/reference/#get-field)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasheetId` | path | `string` | yes | AITable datasheet ID whose fields should be listed. |
