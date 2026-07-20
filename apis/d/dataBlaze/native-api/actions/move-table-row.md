# Move Table Row with Data Blaze

Moves a table row in Data Blaze.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/database/rows/table/6S69TxVQg3kaNMphZCdHyV/{rowId}/move/`
- **Base URL:** `https://data-api.blaze.today`
- **Official documentation:** [Move Table Row](https://blaze.today/datablaze/docs/apis/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rowId` | path | `string` | yes | Mindcloud row ID to move. |
| `before_id` | body | `string` | yes | Move the row before this existing row ID. |
