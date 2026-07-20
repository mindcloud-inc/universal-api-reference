# Get On-Call Calendar with Better Stack Uptime

Retrieves an on-call schedule from Better Stack Uptime.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/on-calls/:scheduleId`
- **Base URL:** `https://uptime.betterstack.com/api`
- **Official documentation:** [Get On-Call Calendar](https://betterstack.com/docs/uptime/api/get-a-single-on-call-calendar/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scheduleId` | path | `string` | yes | On-call schedule ID. Use default for the team default schedule. |
| `date` | query | `string` | no | ISO-8601 date or date-time to inspect the schedule at a specific time. |
