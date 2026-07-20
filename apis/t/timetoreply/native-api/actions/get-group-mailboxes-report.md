# Get Group Mailboxes Report with Timetoreply

## Endpoint

- **Method:** `GET`
- **Path:** `/api/reports/group-mailboxes`
- **Base URL:** `https://portal.timetoreply.com`
- **Official documentation:** [Get Group Mailboxes Report](https://portal.timetoreply.com/api-docs#reports-GETapi-reports-group-mailboxes)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | no | Start date in YYYY-MM-DD format. |
| `model` | query | `string` | no | ID, name, email address, or domain to report on. |
| `model_type` | query | `string` | no | Model type for the selected model. |
| `to` | query | `string` | no | End date in YYYY-MM-DD format. |
