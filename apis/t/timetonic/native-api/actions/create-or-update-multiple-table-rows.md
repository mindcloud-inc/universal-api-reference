# Create Or Update Multiple Table Rows with Timetonic

Creates or updates multiple table rows in Timetonic.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://timetonic.com/live/api.php`
- **Official documentation:** [Create Or Update Multiple Table Rows](https://timetonic.com/live/api.php?doc=#createOrUpdateTableRows-doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `b_o` | body | `string` | yes | Owner of the target TimeTonic book. |
| `rows` | body | `string` | yes | JSON object string keyed by row ids or temporary ids, each containing field id to value mappings. |
| `viewId` | body | `string` | no | Optional view id used when creating or updating rows from a specific view. |
| `tabId` | body | `string` | no | Optional tab id used to scope the batch row request. |
