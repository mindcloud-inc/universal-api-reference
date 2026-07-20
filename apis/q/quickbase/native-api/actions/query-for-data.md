# Query for Data with Quickbase

Queries records from a Quickbase table.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/records/query`
- **Base URL:** `https://api.quickbase.com`
- **Official documentation:** [Query for Data](https://developer.quickbase.com/operation/runQuery)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | The Quickbase table identifier to query. |
| `select[]` | body | `array<number>` | no | Optional array of Quickbase field IDs to return. Leave empty to use the table's default columns. |
| `where` | body | `string` | no | Optional Quickbase query-language filter string, for example {'6'.CT.'Acme'}. |
| `sortBy[]` | body | `array<object>` | no | Optional array of sort objects, each with fieldId and order. |
| `groupBy[]` | body | `array<object>` | no | Optional array of group objects, each with fieldId and grouping. |
| `options` | body | `object` | no | Optional object containing runQuery options such as top, skip, and compareWithAppLocalTime. |
