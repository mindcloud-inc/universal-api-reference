# Update Record with SmartSuite

Updates an existing record in SmartSuite.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/applications/:table_id/records/:record_id/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [Update Record](https://developers.smartsuite.com/docs/solution-data/records/update-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `string` | yes | The SmartSuite table ID that owns the record. |
| `record_id` | path | `string` | yes | The SmartSuite record ID to update. |
| `record` | body | `object` | yes | The SmartSuite record fields to update, keyed by field slug. |
