# Bulk Add Records with SmartSuite

Creates multiple records in SmartSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/applications/:table_id/records/bulk/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [Bulk Add Records](https://developers.smartsuite.com/docs/solution-data/records/bulk-add-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `string` | yes | The SmartSuite table ID that will receive the new records. |
| `items[]` | body | `array<object>` | yes | The list of SmartSuite records to add, keyed by field slug. |
