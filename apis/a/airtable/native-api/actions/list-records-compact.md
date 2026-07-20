# List Records - Compact with Airtable

Retrieves selected fields from records in a specific Airtable table.

## Endpoint

- **Method:** `POST`
- **Path:** `/:baseId/:tableId/listRecords`
- **Base URL:** `https://api.airtable.com/v0`
- **Official documentation:** [List Records - Compact](https://airtable.com/developers/web/api/list-records)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `list<string>` | yes | — |
| `filterByFormula` | body | `string` | no | Leave blank to return all records in this table. If the record has a blank value for one of the fields specified below, the field is omitted from the response. Wrap column names in curly brackets ({}) and use single quotes ('') to wrap string and date values.  Example: {SKU} = '12345' |
| `fields` | body | `list<string>` | yes | The Field Names or Field Id to return in the response. (case-sensitive) Send multiple values as a array. |
| `tableId` | path | `list<string>` | yes | — |
| `offset` | body | `string` | no | — |
