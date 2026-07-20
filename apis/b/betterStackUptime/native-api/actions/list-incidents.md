# List Incidents with Better Stack Uptime

Retrieves incidents from Better Stack Uptime.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/incidents`
- **Base URL:** `https://uptime.betterstack.com/api`
- **Official documentation:** [List Incidents](https://betterstack.com/docs/uptime/api/list-all-incidents/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_name` | query | `string` | no | Filter incidents for a specific Better Stack team when using a global API token. |
| `from` | query | `string` | no | Return incidents from this date (YYYY-MM-DD). |
| `to` | query | `string` | no | Return incidents until this date (YYYY-MM-DD). |
| `monitor_id` | query | `string` | no | Filter incidents for a specific monitor. |
| `heartbeat_id` | query | `string` | no | Filter incidents for a specific heartbeat. |
| `resolved` | query | `boolean` | no | Filter to resolved or unresolved incidents. |
| `acknowledged` | query | `boolean` | no | Filter to acknowledged or unacknowledged incidents. |
