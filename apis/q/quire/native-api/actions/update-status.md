# Update Status with Quire

Updates an existing status in Quire.

## Endpoint

- **Method:** `PUT`
- **Path:** `status/id/:projectId/:value`
- **Base URL:** `https://quire.io/api`
- **Official documentation:** [Update Status](https://quire.io/dev/api/#operation--status-id--projectId---value--put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The project ID or shortcut, for example App_Account. |
| `value` | path | `number` | yes | Current numeric status value to update. |
| `name` | body | `string` | no | Optional updated display name for the status. |
| `value` | body | `number` | no | Optional replacement numeric progress value for the status. |
| `color` | body | `string` | no | Optional updated Quire color code such as 35. |
