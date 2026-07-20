# Delete Status with Quire

Deletes an existing status from Quire.

## Endpoint

- **Method:** `DELETE`
- **Path:** `status/id/:projectId/:value`
- **Base URL:** `https://quire.io/api`
- **Official documentation:** [Delete Status](https://quire.io/dev/api/#operation--status-id--projectId---value--delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The project ID or shortcut, for example App_Account. |
| `value` | path | `number` | yes | Numeric status value to delete. |
