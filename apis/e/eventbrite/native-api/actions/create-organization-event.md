# Create Organization Event with Eventbrite

Creates a new organization event in Eventbrite.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:organizationId/events/`
- **Base URL:** `https://www.eventbriteapi.com/v3`
- **Official documentation:** [Create Organization Event](https://www.eventbrite.com/platform/api#/reference/event/create/create-an-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event.currency` | body | `string` | yes | Event currency code (e.g. USD). |
| `event.end.timezone` | body | `string` | yes | End timezone (e.g. America/Chicago). |
| `event.end.utc` | body | `string` | yes | End datetime in UTC ISO format. |
| `event.name.html` | body | `string` | yes | Event title. |
| `event.start.timezone` | body | `string` | yes | Start timezone (e.g. America/Chicago). |
| `event.start.utc` | body | `string` | yes | Start datetime in UTC ISO format. |
| `organizationId` | path | `string` | yes | Organization identifier. |
