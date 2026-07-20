# List Tables with SmartSuite

Retrieves tables from SmartSuite.

## Endpoint

- **Method:** `GET`
- **Path:** `/applications/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [List Tables](https://developers.smartsuite.com/docs/solution-data/tables/list-tables)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `solution` | query | `string` | no | Filter tables to one SmartSuite solution ID. |
| `fields` | query | `string<string>` | no | Repeat this query argument to request specific table properties from SmartSuite. Send multiple values as a array. |
