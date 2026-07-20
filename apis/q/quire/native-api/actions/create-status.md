# Create Status with Quire

Creates a new status in Quire.

## Endpoint

- **Method:** `POST`
- **Path:** `status/id/:projectId`
- **Base URL:** `https://quire.io/api`
- **Official documentation:** [Create Status](https://quire.io/dev/api/#operation--status-id--projectId--post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The project ID or shortcut, for example App_Account. |
| `name` | body | `string` | yes | Display name of the new status. |
| `value` | body | `number` | yes | Unique numeric progress value for the new status. |
| `color` | body | `string` | no | Optional Quire color code such as 35. |
