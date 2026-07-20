# Create Record with SmartSuite

Creates a new record in SmartSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/applications/:table_id/records/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [Create Record](https://developers.smartsuite.com/docs/solution-data/records/create-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `string` | yes | The SmartSuite table ID that will receive the new record. |
| `record` | body | `object` | yes | The SmartSuite record payload keyed by field slug. |
