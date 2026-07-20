# List Event Attendees with Explara

Retrieves event attendees from Explara.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/e/attendee-list`
- **Base URL:** `https://www.explara.com`
- **Official documentation:** [List Event Attendees](https://developers.explara.com/developers-api#11-event-attendee-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | body | `string` | yes | Explara event identifier. |
| `fromRecord` | body | `number` | yes | Starting attendee record number. |
| `toRecord` | body | `number` | yes | Ending attendee record number. |
