# List Conversation Logs with Timetoreply

## Endpoint

- **Method:** `GET`
- **Path:** `/api/logs/conversations`
- **Base URL:** `https://portal.timetoreply.com`
- **Official documentation:** [List Conversation Logs](https://portal.timetoreply.com/api-docs#logs-GETapi-logs-conversations)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | no | Start date in YYYY-MM-DD format. |
| `model` | query | `string` | no | ID, name, email address, or domain to report on. |
| `model_type` | query | `string` | no | Model type for the selected model. |
| `search` | query | `string` | no | Search for a specific email subject line. |
| `to` | query | `string` | no | End date in YYYY-MM-DD format. |
