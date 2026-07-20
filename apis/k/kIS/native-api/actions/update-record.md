# Update Record with KIS

Updates an existing record in a KIS data table.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api_token_access/data_handlers/{recordId}`
- **Base URL:** `https://api.getkis.io/api/v1`
- **Official documentation:** [Update Record](https://doc.kis.work/documentation/documentation-api/donnees-dune-table-de-donnees/mettre-a-jour-une-donnee)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recordId` | path | `string` | yes | KIS object ID for the record to update. Used in the request path. |
| `collection_name` | body | `string` | yes | Exact KIS table name containing the record. |
| `documents[]` | body | `array<object>` | yes | Single-item array containing the record _id and fields to update. |
