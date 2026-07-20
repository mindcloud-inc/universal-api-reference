# Edit Table Value Comments with Timetonic

Updates comments for a table value in Timetonic.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://timetonic.com/live/api.php`
- **Official documentation:** [Edit Table Value Comments](https://timetonic.com/live/api.php?doc=#editTableValueComments-doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `b_o` | body | `string` | yes | Book owner containing the row. |
| `rowId` | body | `string` | yes | Row identifier containing the field value. |
| `fieldId` | body | `string` | yes | Field identifier whose comment should be edited. |
| `commentId` | body | `string` | yes | Comment identifier to edit. |
| `comment` | body | `string` | yes | Updated comment text. |
