# Get Time Off Requests with BambooHR

Retrieves time off requests from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time_off/requests`
- **Base URL:** `https://mindcloud.bamboohr.com/api`
- **Official documentation:** [Get Time Off Requests](https://documentation.bamboohr.com/reference/time-off-get-time-off-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | query | `string` | yes | End date for the request window in YYYY-MM-DD format. |
| `start` | query | `string` | yes | Start date for the request window in YYYY-MM-DD format. |
