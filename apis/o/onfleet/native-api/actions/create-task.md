# Create Task with Onfleet

Creates a new task in Onfleet.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://onfleet.com/api/v2`
- **Official documentation:** [Create Task](https://docs.onfleet.com/reference/create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destination` | body | `string` | yes | The ID of the task destination. |
| `recipients[]` | body | `array<string>` | no | An array containing zero or one recipient IDs. |
| `completeAfter` | body | `number` | no | Earliest completion time as a Unix timestamp in milliseconds. |
| `completeBefore` | body | `number` | no | Latest completion time as a Unix timestamp in milliseconds. |
| `pickupTask` | body | `boolean` | no | Whether the task is a pickup task. |
| `notes` | body | `string` | no | Optional notes for the task. |
| `quantity` | body | `number` | no | The number of units to be dropped off while completing this task. |
| `serviceTime` | body | `number` | no | The number of minutes a worker should spend on arrival at this task's destination. |
| `recipientName` | body | `string` | no | Optional recipient name override for this task only. |
| `recipientNotes` | body | `string` | no | Optional recipient notes override for this task only. |
| `recipientSkipSMSNotifications` | body | `boolean` | no | Optional recipient SMS notification override for this task only. |
