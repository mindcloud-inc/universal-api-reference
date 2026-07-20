# Update Checklist with Checkvist

Updates a checklist in Checkvist.

## Endpoint

- **Method:** `PUT`
- **Path:** `/checklists/:checklistId.json`
- **Base URL:** `https://checkvist.com`
- **Official documentation:** [Update Checklist](https://checkvist.com/auth/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checklist.name` | body | `string` | no | The checklist name. |
| `checklist.public` | body | `boolean` | no | Set to 1 to make the checklist public. |
| `checklistId` | path | `number` | yes | The checklist ID. |
