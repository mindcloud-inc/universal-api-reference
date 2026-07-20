# Delete Record with SmartSuite

Deletes an existing record from SmartSuite.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/applications/:table_id/records/:record_id/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [Delete Record](https://developers.smartsuite.com/docs/solution-data/records/delete-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `string` | yes | The SmartSuite table ID that owns the record. |
| `record_id` | path | `string` | yes | The SmartSuite record ID to delete. |
