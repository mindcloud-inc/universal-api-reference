# List Deleted Records with SmartSuite

Retrieves deleted records from SmartSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/deleted-records/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [List Deleted Records](https://developers.smartsuite.com/docs/solution-data/records/list-deleted-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `solution_id` | body | `string` | yes | The SmartSuite solution ID whose deleted records should be listed. |
