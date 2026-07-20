# List Records with AITable.ai

Retrieves records from a datasheet in AITable.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/fusion/v1/datasheets/:datasheetId/records`
- **Base URL:** `https://aitable.ai`
- **Official documentation:** [List Records](https://developers.aitable.ai/api/reference/#get-records)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasheetId` | path | `string` | yes | AITable datasheet ID, for example dst0Yj5aNeoHldqvf6. |
| `viewId` | query | `string` | no | Optional view ID. When provided, AITable returns fields visible in that view. |
| `fieldKey` | query | `string` | no | Use field names or field IDs when returning fields. AITable supports name or id. |
| `maxRecords` | query | `number` | no | Optional maximum number of records to return. |
