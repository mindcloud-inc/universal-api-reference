# Get Who's Out with BambooHR

Retrieves who's out entries and holidays from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time_off/whos_out`
- **Base URL:** `https://mindcloud.bamboohr.com/api`
- **Official documentation:** [Get Who's Out](https://documentation.bamboohr.com/reference/get-a-list-of-who-is-out-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | query | `string` | yes | End date for the window in YYYY-MM-DD format. |
| `start` | query | `string` | yes | Start date for the window in YYYY-MM-DD format. |
