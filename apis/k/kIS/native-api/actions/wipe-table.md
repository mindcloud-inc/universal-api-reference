# Wipe Table with KIS

Deletes all records from a KIS data table.

## Endpoint

- **Method:** `POST`
- **Path:** `/api_token_access/collections/wipe/{tableId}`
- **Base URL:** `https://api.getkis.io/api/v1`
- **Official documentation:** [Wipe Table](https://doc.kis.work/documentation/documentation-api/donnees-dune-table-de-donnees/supprimer-la-totalite-des-donnees-dune-table-de-donnees)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableId` | path | `string` | yes | KIS table object ID to wipe. Used in the request path. |
