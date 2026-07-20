# Mark Time Entries as Invoiced with Clockify

Marks time entries as invoiced in Clockify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `workspaces/:workspaceId/time-entries/invoiced`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Mark Time Entries as Invoiced](https://docs.developer.clockify.me/#tag/Time-entry/operation/updateInvoicedStatus)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `invoiced` | body | `boolean` | yes |
| `timeEntryIds[]` | body | `array<object>` | yes |
| `timeEntryIds[].dateOfCreationFromObjectId` | body | `date` | no |
