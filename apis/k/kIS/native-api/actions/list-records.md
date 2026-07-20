# List Records with KIS

Retrieves all records from a KIS data table.

## Endpoint

- **Method:** `POST`
- **Path:** `/api_token_access/data_handlers`
- **Base URL:** `https://api.getkis.io/api/v1`
- **Official documentation:** [List Records](https://doc.kis.work/documentation/documentation-api/donnees-dune-table-de-donnees/recuperer-les-donnees)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_name` | body | `string` | yes | Exact KIS table name to query. |
| `limit` | body | `number` | no | Maximum number of records to return. |
