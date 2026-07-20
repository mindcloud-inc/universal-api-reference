# List Event Instances with Google Calendar

Retrieves recurring event instances from Google Calendar.

## Endpoint

- **Method:** `GET`
- **Path:** `calendars/:calendar/events/:eventId/instances`
- **Base URL:** `https://www.googleapis.com/calendar/v3`
- **Official documentation:** [List Event Instances](https://developers.google.com/workspace/calendar/api/v3/reference/events/instances)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `calendar` | path | `list` | no |
| `eventId` | path | `string` | no |
