# List Organization Venues with Eventbrite

Retrieves organization venues from Eventbrite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/venues/`
- **Base URL:** `https://www.eventbriteapi.com/v3`
- **Official documentation:** [List Organization Venues](https://www.eventbrite.com/platform/api#/reference/venue/list/list-venues-by-organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Organization identifier. |
