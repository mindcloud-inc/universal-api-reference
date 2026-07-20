# Get Available Slots with Cal.com

Retrieves available slots from Cal.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/slots`
- **Base URL:** `https://api.cal.com/v2`
- **Official documentation:** [Get Available Slots](https://cal.com/docs/api-reference/v2/slots/get-available-time-slots-for-an-event-type)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookingUidToReschedule` | query | `list` | no | Existing booking UID when requesting slots for rescheduling. |
| `duration` | query | `number` | no | Requested slot duration in minutes. |
| `eventTypeId` | query | `list` | no | Event type ID to resolve slots. |
| `eventTypeSlug` | query | `list` | no | Event type slug to resolve slots. |
| `format` | query | `list` | no | Response slot format option. Accepted values: `range`, `time`. |
| `organizationSlug` | query | `string` | no | Organization slug for event type lookup. |
| `start` | query | `string` | yes | Range start in ISO 8601 UTC format. |
| `teamSlug` | query | `string` | no | Team slug for event type lookup. |
| `timeZone` | query | `string` | no | IANA time zone for slot rendering. |
| `username` | query | `string` | no | Username for user-scoped event type lookup. |
| `usernames` | query | `string` | no | Comma-separated usernames for team lookup. |
| `end` | query | `string` | yes | Range end in ISO 8601 UTC format. |
