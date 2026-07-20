# List Agent Alerts with Timetoreply

## Endpoint

- **Method:** `GET`
- **Path:** `/api/reports/alerts/:agent_id`
- **Base URL:** `https://portal.timetoreply.com`
- **Official documentation:** [List Agent Alerts](https://portal.timetoreply.com/api-docs#reports-GETapi-reports-alerts--agent_id-)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `number` | yes | Agent identifier from the alert route. |
| `days` | query | `number` | no | Number of days of alerts to include. |
