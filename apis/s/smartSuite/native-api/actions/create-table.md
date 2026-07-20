# Create Table with SmartSuite

Creates a new table in SmartSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/applications/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [Create Table](https://developers.smartsuite.com/docs/solution-data/tables/create-table)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `solution` | body | `string` | yes | The SmartSuite solution ID that will own the new table. |
| `name` | body | `string` | yes | The display name for the new SmartSuite table. |
| `structure[]` | body | `array<object>` | yes | An array of SmartSuite field definitions to create with the new table. |
