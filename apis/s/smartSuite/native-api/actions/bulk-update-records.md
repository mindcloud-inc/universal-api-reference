# Bulk Update Records with SmartSuite

Updates existing records in SmartSuite in bulk.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/applications/:table_id/records/bulk/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [Bulk Update Records](https://developers.smartsuite.com/docs/solution-data/records/bulk-update-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `string` | yes | The SmartSuite table ID that owns the records. |
| `items[]` | body | `array<object>` | yes | The list of SmartSuite record updates including each record ID. |
