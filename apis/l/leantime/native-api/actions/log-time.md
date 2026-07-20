# Log Time with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [Log Time](https://docs.leantime.io/api/classes/Leantime/Domain/Timesheets/Services/Timesheets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | body | `number` | yes | The ticket to log time against. |
| `kind` | body | `string` | yes | The timesheet entry type. |
| `hours` | body | `number` | yes | The number of hours to add. |
| `timestamp` | body | `number` | yes | Unix timestamp for the work date. |
| `description` | body | `string` | no | Optional timesheet description. |
