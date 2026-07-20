# Delete Table Value Comments with Timetonic

Deletes comments for a table value from Timetonic.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://timetonic.com/live/api.php`
- **Official documentation:** [Delete Table Value Comments](https://timetonic.com/live/api.php?doc=#deleteTableValueComments-doc)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `b_o` | body | `string` | yes |
| `rowId` | body | `string` | yes |
| `fieldId` | body | `string` | yes |
| `commentId` | body | `string` | yes |
