# Create Or Update Table Row with Timetonic

Creates or updates a table row in Timetonic.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://timetonic.com/live/api.php`
- **Official documentation:** [Create Or Update Table Row](https://timetonic.com/live/api.php?doc=#createOrUpdateTableRow-doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `b_o` | body | `string` | yes | Owner of the target TimeTonic book. |
| `rowId` | body | `string` | yes | Existing row id to update, or tmpNEW_ROW to create a new row. |
| `fieldValues` | body | `string` | yes | JSON object string mapping field ids to row values. |
| `viewId` | body | `string` | no | Optional view id used when creating or updating the row from a specific view. |
| `tabId` | body | `string` | no | Optional tab id used to scope the row request. |
| `linkSeparator` | body | `string` | no | Optional separator for link-type values. |
| `bypassUrlTrigger` | body | `string` | no | Optional flag to disable webhooks for this mutation. |
