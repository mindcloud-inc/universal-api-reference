# Rollback Change On A Row with Timetonic

Rolls back a row change in Timetonic.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://timetonic.com/live/api.php`
- **Official documentation:** [Rollback Change On A Row](https://timetonic.com/live/api.php?doc=#rollBackBeforeChange-doc)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `b_o` | body | `string` | yes |
| `catId` | body | `string` | no |
| `rowId` | body | `string` | yes |
