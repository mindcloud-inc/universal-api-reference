# Get Table Value Subset with Timetonic

Retrieves a subset of table values from Timetonic.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://timetonic.com/live/api.php`
- **Official documentation:** [Get Table Value Subset](https://timetonic.com/live/api.php?doc=#getTableValueSubset-doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `b_o` | body | `string` | yes | Owner of the target book. |
| `catId` | body | `string` | yes | Table/category id to read from. |
| `fieldIds` | body | `string` | yes | Comma-separated field ids to return. |
| `rowIds` | body | `string` | yes | Comma-separated row ids to return. |
