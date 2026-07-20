# Send Reminder with SigningHub

Sends a workflow reminder in SigningHub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/packages/:packageId/workflow/:order/remind`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Send Reminder](https://manuals.ascertia.com/SigningHub/10.0/Api/#tag/Document-Workflow/operation/Reminder_SendReminder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order` | path | `number` | yes | Workflow order to remind. |
| `packageId` | path | `number` | yes | Package ID of the workflow package. |
