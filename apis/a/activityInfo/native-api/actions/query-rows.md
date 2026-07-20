# Query Rows with ActivityInfo

Queries rows from ActivityInfo form data.

## Endpoint

- **Method:** `POST`
- **Path:** `/resources/query/rows`
- **Base URL:** `https://www.activityinfo.org`
- **Official documentation:** [Query Rows](https://www.activityinfo.org/support/docs/api/reference/queryRows.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rowSources[]` | body | `array<object>` | yes | Forms to query as row sources. |
| `columns[]` | body | `array<object>` | yes | Columns to return. |
