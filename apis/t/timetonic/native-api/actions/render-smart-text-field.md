# Render Smart Text Field with Timetonic

Retrieves rendered output for a smart text field from Timetonic.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://timetonic.com/live/api.php`
- **Official documentation:** [Render Smart Text Field](https://timetonic.com/live/api.php?doc=#renderSmartTextField-doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `b_o` | body | `string` | yes | Book owner containing the row. |
| `catId` | body | `string` | yes | Category or table identifier. |
| `rowId` | body | `string` | yes | Row identifier containing the field value. |
| `fieldId` | body | `string` | yes | Field identifier to render. |
