# Create On-Call Calendar with Better Stack Uptime

Creates a new on-call schedule in Better Stack Uptime.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/on-calls`
- **Base URL:** `https://uptime.betterstack.com/api`
- **Official documentation:** [Create On-Call Calendar](https://betterstack.com/docs/uptime/api/create-on-call-calendar/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | On-call schedule name. |
| `team_name` | body | `string` | no | Better Stack team name when required by the token scope. |
