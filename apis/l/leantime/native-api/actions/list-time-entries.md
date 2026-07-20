# List Time Entries with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [List Time Entries](https://docs.leantime.io/api/classes/Leantime/Domain/Timesheets/Services/Timesheets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateFrom` | body | `string` | yes | Start of the reporting range. |
| `dateTo` | body | `string` | yes | End of the reporting range. |
