# Get Table Value Comments with Timetonic

Retrieves comments for a table value from Timetonic.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://timetonic.com/live/api.php`
- **Official documentation:** [Get Table Value Comments](https://timetonic.com/live/api.php?doc=#getTableValueComments-doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `b_o` | body | `string` | yes | Book owner containing the row. |
| `rowId` | body | `string` | yes | Row identifier containing the field value. |
| `fieldId` | body | `string` | yes | Field identifier whose comments should be fetched. |
