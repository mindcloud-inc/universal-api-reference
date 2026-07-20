# List Sheets with Smartsheet

Retrieves sheets from Smartsheet.

## Endpoint

- **Method:** `GET`
- **Path:** `/sheets`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [List Sheets](https://developers.smartsheet.com/api/smartsheet/openapi/sheets/list-sheets)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | no | Optional response elements to include in each sheet record. |
| `includeAll` | query | `boolean` | no | — |
| `modifiedSince` | query | `date` | no | Only return sheets modified on or after this date and time. |
| `numericDates` | query | `boolean` | no | — |
