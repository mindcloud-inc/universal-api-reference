# Export Job Notes with ServiceTitan

## Endpoint

- **Method:** `GET`
- **Path:** `jpm/v2/tenant/{tenant}/export/job-notes`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Export Job Notes](https://developer.servicetitan.io/api-details/#api=tenant-jpm-v2&operation=Export_JobNotes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | no | Continuation token received from previous export request in "continueFrom" field. When not specified, the export process starts from the beginning. Use custom date strings, e.g. "2020-01-01" to start the export process from the certain point in time. |
| `includeRecentChanges` | query | `boolean` | no | Format: `toggle`. |
