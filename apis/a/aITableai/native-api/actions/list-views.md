# List Views with AITable.ai

Retrieves views from a datasheet in AITable.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/fusion/v1/datasheets/:datasheetId/views`
- **Base URL:** `https://aitable.ai`
- **Official documentation:** [List Views](https://developers.aitable.ai/api/reference/#get-view)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasheetId` | path | `string` | yes | AITable datasheet ID whose views should be listed. |
