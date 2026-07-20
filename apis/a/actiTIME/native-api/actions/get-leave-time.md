# Get Leave Time with actiTIME

Retrieves leave time records from actiTIME by date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/leavetime`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Get Leave Time](https://www.actitime.com/api-documentation/leave-time-resource)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateFrom` | query | `string` | yes | Start date of requested leave time in YYYY-MM-DD format. |
| `dateTo` | query | `string` | no | End date of requested leave time in YYYY-MM-DD format. |
| `includeReferenced` | query | `string` | no | Comma-separated referenced objects to include. |
| `leaveTypeIds` | query | `string` | no | Comma-separated leave type ids. |
| `stopAfter` | query | `number` | no | Approximate number of leave time records to return. |
| `userIds` | query | `string` | no | Comma-separated user ids. |
