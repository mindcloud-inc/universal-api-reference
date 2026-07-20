# Bulk Delete Records with SmartSuite

Deletes existing records from SmartSuite in bulk.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/applications/:tableId/records/bulk_delete/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [Bulk Delete Records](https://developers.smartsuite.com/docs/solution-data/records/bulk-delete-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableId` | path | `string` | yes | The SmartSuite table ID that owns the records. |
| `items[]` | body | `array<string>` | yes | Up to 25 SmartSuite record IDs to soft-delete. |
