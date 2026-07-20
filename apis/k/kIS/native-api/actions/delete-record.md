# Delete Record with KIS

Deletes an existing record from a KIS data table.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api_token_access/data_handlers/{recordId}`
- **Base URL:** `https://api.getkis.io/api/v1`
- **Official documentation:** [Delete Record](https://doc.kis.work/documentation/documentation-api/donnees-dune-table-de-donnees/supprimer-une-donnee)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recordId` | path | `string` | yes | KIS object ID for the record to delete. Used in the request path. |
| `collection_name` | body | `string` | yes | Exact KIS table name containing the record. |
| `document_id` | body | `string` | yes | KIS object ID for the record to delete. Must match the path record ID. |
