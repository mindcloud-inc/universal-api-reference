# List Events with Google Calendar

Retrieves events from a Google Calendar calendar.

## Endpoint

- **Method:** `GET`
- **Path:** `calendars/:calendar/events`
- **Base URL:** `https://www.googleapis.com/calendar/v3`
- **Official documentation:** [List Events](https://developers.google.com/workspace/calendar/api/v3/reference/events/list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendar` | path | `list` | yes | — |
| `timeMin` | query | `date` | no | Lower bound (exclusive) for an event's end time to filter by. |
| `timeMax` | query | `date` | no | Upper bound (exclusive) for an event's start time to filter by. |
| `q` | query | `string` | no | — |
| `updatedMin` | query | `date` | no | Lower bound for an event's last modification time to filter by. |
| `showDeleted` | query | `boolean` | no | Format: `toggle`. |
| `showHiddenInvitations` | query | `boolean` | no | Format: `toggle`. |
| `singleEvents` | query | `boolean` | no | Whether to expand recurring events into instances and only return single one-off events and instances of recurring events, but not the underlying recurring events themselves. Optional. The default is False. Format: `toggle`. |
