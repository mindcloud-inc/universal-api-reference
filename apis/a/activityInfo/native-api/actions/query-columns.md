# Query Columns with ActivityInfo

Queries column data from ActivityInfo form sources.

## Endpoint

- **Method:** `POST`
- **Path:** `/resources/query/columns`
- **Base URL:** `https://www.activityinfo.org`
- **Official documentation:** [Query Columns](https://www.activityinfo.org/support/docs/api/reference/queryColumns.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rowSources[]` | body | `array<object>` | yes | Forms to query as row sources. |
| `columns[]` | body | `array<object>` | yes | Columns to return. |
