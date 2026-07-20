# List Events with Flexopus

Retrieves a list of events from Flexopus.

## Endpoint

- **Method:** `GET`
- **Path:** `/events`
- **Base URL:** `{tenantBaseUrl}/api/v1`
- **Official documentation:** [List Events](https://flexopus.com/api/docs/#endpoints-GETapi-v1-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `date` | yes | Start of the event window as an ISO timestamp. |
| `to` | query | `date` | yes | End of the event window as an ISO timestamp. |
| `building_id` | query | `number` | no | Identifier of the building to show events for. |
| `location_id` | query | `number` | no | Identifier of the location to show events for. |
| `bookable_id` | query | `number` | no | Identifier of the bookable to show events for. |
