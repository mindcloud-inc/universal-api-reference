# List Booked Slots with Datelist

Retrieves booked slots from Datelist by email, calendar, or date.

## Endpoint

- **Method:** `GET`
- **Path:** `/booked_slots`
- **Base URL:** `https://datelist.io/api`
- **Official documentation:** [List Booked Slots](https://apidoc.datelist.io/booked_slots)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Only return booked slots matching a specific email. |
| `calendar_id` | query | `number` | no | Only return booked slots for a specific calendar. |
| `from` | query | `string` | no | Only return booked slots starting from this ISO 8601 date-time. |
| `to` | query | `string` | no | Only return booked slots up to this ISO 8601 date-time. |
