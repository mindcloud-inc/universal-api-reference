# Add Shift with Deputy

Creates a new shift in Deputy.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/supervise/roster`
- **Base URL:** `https://{endpoint}.deputy.com`
- **Official documentation:** [Add Shift](https://developer.deputy.com/docs/adding-a-shift)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `intStartTimestamp` | body | `number` | no | Start time of the shift in unix timestamp format. |
| `intEndTimestamp` | body | `number` | no | End time of the shift in unix timestamp format. |
| `intRosterEmployee` | body | `number` | no | Id of the employee working the shift when the shift is filled. |
| `blnPublish` | body | `boolean` | no | Whether the shift should be published. |
| `intMealbreakMinute` | body | `number` | no | Number of minutes to include as a meal break. |
| `intOpunitId` | body | `number` | no | The location or area id for the shift. |
| `blnForceOverwrite` | body | `number` | no | Whether to force overwrite with 0 or 1. |
| `blnOpen` | body | `number` | no | Whether the shift is open using 0 or 1. |
| `strComment` | body | `string` | no | Comment text on the shift. |
| `intConfirmStatus` | body | `number` | no | Whether the employee's shift should be confirmed with 1 or 0. |
