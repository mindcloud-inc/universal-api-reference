# Get Activity Events with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `admin/activityevents`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Activity Events](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/get-activity-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | Filters the results based on a boolean condition, using 'Activity', 'UserId', or both properties. Supports only 'eq' and 'and' operators. |
| `continuationToken` | query | `string` | no | Token required to get the next chunk of the result set |
| `endDateTime` | query | `string` | no | End date and time of the window for audit event results. Must be in ISO 8601 compliant UTC format. |
| `startDateTime` | query | `string` | no | Start date and time of the window for audit event results. Must be in ISO 8601 compliant UTC format. |
