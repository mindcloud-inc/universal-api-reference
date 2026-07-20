# Restore Deleted Record with SmartSuite

Restores a deleted record in SmartSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/deleted-records/:recordId/restore/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [Restore Deleted Record](https://developers.smartsuite.com/docs/solution-data/records/restore-deleted-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recordId` | path | `string` | yes | The deleted SmartSuite record ID from the deleted-records API. SmartSuite documents this path token as record_id. |
