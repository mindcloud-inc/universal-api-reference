# List Events with Sympla

Retrieves the organizer's events from Sympla.

## Endpoint

- **Method:** `GET`
- **Path:** `/events`
- **Base URL:** `https://api.sympla.com.br/public/v1.5.1`
- **Official documentation:** [List Events](https://developers.sympla.com.br/api-doc/index.html#operation/getAllEvent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | no | Filter events that start on or after this datetime in YYYY-MM-DD HH:mm:ss format. |
| `published` | query | `boolean` | no | When true, only published events are returned. |
| `fields` | query | `string` | no | Optional comma-separated response fields to include. |
