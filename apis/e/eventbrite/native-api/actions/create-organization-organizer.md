# Create Organization Organizer with Eventbrite

Creates a new organization organizer in Eventbrite.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:organizationId/organizers/`
- **Base URL:** `https://www.eventbriteapi.com/v3`
- **Official documentation:** [Create Organization Organizer](https://www.eventbrite.com/platform/docs/organizations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Organization identifier. |
| `organizer.name` | body | `string` | yes | Organizer display name. |
