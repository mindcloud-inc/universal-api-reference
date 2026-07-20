# Get Record with SmartSuite

Retrieves a record from SmartSuite.

## Endpoint

- **Method:** `GET`
- **Path:** `/applications/:table_id/records/:record_id/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [Get Record](https://developers.smartsuite.com/docs/solution-data/records/get-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `string` | yes | The SmartSuite table ID that owns the record. |
| `record_id` | path | `string` | yes | The SmartSuite record ID to fetch. |
| `hydrated` | query | `boolean` | no | Return hydrated values when SmartSuite supports hydration for the table. |
