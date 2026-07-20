# Get Records For View with SmartSuite

Retrieves records for a SmartSuite view.

## Endpoint

- **Method:** `GET`
- **Path:** `/applications/:tableId/records-for-report/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [Get Records For View](https://developers.smartsuite.com/docs/solution-data/views/records-for-view)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableId` | path | `string` | yes | The SmartSuite table ID that owns the view. |
| `report` | query | `string` | yes | The SmartSuite report or view ID to read records from. |
| `with_empty_values` | query | `boolean` | no | Whether SmartSuite should include empty field values in the record payload. |
