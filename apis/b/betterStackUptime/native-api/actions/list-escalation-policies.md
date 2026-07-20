# List Escalation Policies with Better Stack Uptime

Retrieves escalation policies from Better Stack Uptime.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/policies`
- **Base URL:** `https://uptime.betterstack.com/api`
- **Official documentation:** [List Escalation Policies](https://betterstack.com/docs/uptime/api/list-all-escalation-policies/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_name` | query | `string` | no | Better Stack team name when required by the token scope. |
