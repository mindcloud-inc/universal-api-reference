# Duplicate Solution with SmartSuite

Creates a duplicate of a solution in SmartSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/solutions/duplicate/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [Duplicate Solution](https://developers.smartsuite.com/docs/solution-data/solutions/duplicate-solution)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `solution_id` | body | `string` | yes | The SmartSuite solution ID to duplicate. |
| `name` | body | `string` | yes | The name for the duplicated SmartSuite solution. |
| `from_workspace` | body | `string` | yes | The source SmartSuite workspace ID. |
| `to_workspace` | body | `string` | yes | The destination SmartSuite workspace ID. |
| `copy_records` | body | `boolean` | no | Whether SmartSuite should copy records into the duplicated solution. |
| `copy_comments` | body | `boolean` | no | Whether SmartSuite should copy comments into the duplicated solution. |
