# List Reminders with Zoom Team Chat

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/reminder`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [List Reminders](https://developers.zoom.us/docs/api/rest/reference/chat/methods/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to_contact` | query | `string` | no | The contact email address for reminders. |
| `to_channel` | query | `string` | no | The channel ID for reminders. |
