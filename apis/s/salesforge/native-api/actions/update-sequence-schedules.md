# Update Sequence Schedules with Salesforge

Updates sequence schedules in Salesforge.

## Endpoint

- **Method:** `PUT`
- **Path:** `/public/v2/workspaces/:workspaceID/sequences/:sequenceID/schedules`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [Update Sequence Schedules](https://api.salesforge.ai/public/v2/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes | Workspace ID for the sequence. |
| `sequenceID` | path | `string` | yes | Sequence ID to update schedules for. |
| `schedules[]` | body | `array<object>` | yes | Array of weekday schedules with fromHour and toHour. |
