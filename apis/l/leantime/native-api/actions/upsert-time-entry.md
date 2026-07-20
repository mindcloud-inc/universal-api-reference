# Upsert Time Entry with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [Upsert Time Entry](https://docs.leantime.io/api/classes/Leantime/Domain/Timesheets/Services/Timesheets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | body | `number` | yes | The ticket to upsert time against. |
| `kind` | body | `string` | yes | The timesheet entry type. |
| `hours` | body | `number` | yes | The number of hours to set. |
| `timestamp` | body | `number` | yes | Unix timestamp for the work date. |
