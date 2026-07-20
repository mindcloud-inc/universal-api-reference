# List Organization Attendees with Eventbrite

Retrieves organization attendees from Eventbrite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/attendees/`
- **Base URL:** `https://www.eventbriteapi.com/v3`
- **Official documentation:** [List Organization Attendees](https://www.eventbrite.com/platform/api#/reference/attendee/list/list-attendees-by-organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Organization identifier. |
