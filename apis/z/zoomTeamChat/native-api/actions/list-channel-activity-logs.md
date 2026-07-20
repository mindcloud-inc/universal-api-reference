# List Channel Activity Logs with Zoom Team Chat

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/channels/:channelId/activities`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [List Channel Activity Logs](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/listChannelActivityLogs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | The channel's unique identifier. |
| `activity_type` | query | `string` | no | The activity log type. |
| `start_date` | query | `string` | yes | The activity log start date in YYYY-MM-DD format. |
| `end_date` | query | `string` | yes | The activity log end date in YYYY-MM-DD format. |
