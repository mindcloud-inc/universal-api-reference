# Delete Field(s) with Quickbase

Deletes existing fields from a Quickbase table.

## Endpoint

- **Method:** `DELETE`
- **Path:** `v1/fields`
- **Base URL:** `https://api.quickbase.com`
- **Official documentation:** [Delete Field(s)](https://developer.quickbase.com/operation/deleteFields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableId` | query | `string` | yes | The Quickbase table that contains the fields to delete. |
| `fieldIds[]` | body | `array<number>` | yes | The list of Quickbase field IDs to delete. |
