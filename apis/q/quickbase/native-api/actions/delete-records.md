# Delete Record(s) with Quickbase

Deletes records from a Quickbase table.

## Endpoint

- **Method:** `DELETE`
- **Path:** `v1/records`
- **Base URL:** `https://api.quickbase.com`
- **Official documentation:** [Delete Record(s)](https://developer.quickbase.com/operation/deleteRecords)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | The Quickbase table identifier. |
| `where` | body | `string` | yes | Quickbase where clause that selects the records to delete. |
