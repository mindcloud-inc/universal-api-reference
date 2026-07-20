# Create Action Item with IceCubes

## Endpoint

- **Method:** `POST`
- **Path:** `/action-items`
- **Base URL:** `https://icecubes.app/api/public`
- **Official documentation:** [Create Action Item](https://icecubes.app/docs/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meetingId` | body | `string` | yes | The meeting ID to attach the action item to. |
| `text` | body | `string` | yes | The action item text. |
| `assigneeEmail` | body | `string` | no | Assign the action item to an email address. |
| `dueDate` | body | `date` | no | Optional due date in ISO 8601 format. |
