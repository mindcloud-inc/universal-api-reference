# Get Time Track with actiTIME

Retrieves time track records from actiTIME by date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/timetrack`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Get Time Track](https://www.actitime.com/api-documentation/time-track-resource)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `approved` | query | `boolean` | no | Filter approved vs not-approved time track. |
| `customerIds` | query | `string` | no | Comma-separated customer ids. |
| `dateFrom` | query | `string` | yes | Start date of requested time track in YYYY-MM-DD format. |
| `dateTo` | query | `string` | no | End date of requested time track in YYYY-MM-DD format. |
| `includeReferenced` | query | `string` | no | Comma-separated referenced objects to include. |
| `projectIds` | query | `string` | no | Comma-separated project ids. |
| `stopAfter` | query | `number` | no | Approximate number of time-track records to return. |
| `taskIds` | query | `string` | no | Comma-separated task ids. |
| `userIds` | query | `string` | no | Comma-separated user ids. |
