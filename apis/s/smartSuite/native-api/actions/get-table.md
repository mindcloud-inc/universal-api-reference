# Get Table with SmartSuite

Retrieves a table from SmartSuite.

## Endpoint

- **Method:** `GET`
- **Path:** `/applications/:table_id/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [Get Table](https://developers.smartsuite.com/docs/solution-data/tables/get-table)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `string` | yes | The SmartSuite table ID to fetch. |
| `fields` | query | `string<string>` | no | Repeat this query argument to request specific table properties from SmartSuite. Send multiple values as a array. |
