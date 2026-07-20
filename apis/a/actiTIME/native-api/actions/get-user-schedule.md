# Get User Schedule with actiTIME

Retrieves a user's schedule from actiTIME.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:uid/schedule`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Get User Schedule](https://www.actitime.com/api-documentation/users-resource)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateFrom` | query | `string` | no | Start date of requested schedule in YYYY-MM-DD format. |
| `dateTo` | query | `string` | no | End date of requested schedule in YYYY-MM-DD format. |
| `uid` | path | `string` | yes | User ID or username. |
