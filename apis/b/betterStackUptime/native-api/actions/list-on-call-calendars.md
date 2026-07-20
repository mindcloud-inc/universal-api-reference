# List On-Call Calendars with Better Stack Uptime

Retrieves on-call schedules from Better Stack Uptime.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/on-calls`
- **Base URL:** `https://uptime.betterstack.com/api`
- **Official documentation:** [List On-Call Calendars](https://betterstack.com/docs/uptime/api/list-all-existing-on-call-calendars/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_name` | query | `string` | no | Better Stack team name when required by the token scope. |
