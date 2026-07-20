# Create Records with KIS

Creates one or more records in a KIS data table.

## Endpoint

- **Method:** `POST`
- **Path:** `/api_token_access/data_handlers`
- **Base URL:** `https://api.getkis.io/api/v1`
- **Official documentation:** [Create Records](https://doc.kis.work/documentation/documentation-api/donnees-dune-table-de-donnees/creer-de-la-donnee)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_name` | body | `string` | yes | Exact KIS table name where records should be created. |
| `documents[]` | body | `array<object>` | yes | Array of objects to create. Keys must match the KIS table field names exactly. |
