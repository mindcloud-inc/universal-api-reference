# Update Table Row with Data Blaze

Updates an existing table row in Data Blaze.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/database/rows/table/6S69TxVQg3kaNMphZCdHyV/{rowId}/`
- **Base URL:** `https://data-api.blaze.today`
- **Official documentation:** [Update Table Row](https://blaze.today/datablaze/docs/apis/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rowId` | path | `string` | yes | Mindcloud row ID. |
| `field_028bLj7zLab3TYslzthhXu` | body | `string` | no | Updated value for the Mindcloud Name field. |
| `field_2Te3k3Sf4edLQ3a0WE2a8J` | body | `number` | no | Updated value for the Mindcloud Count field. |
