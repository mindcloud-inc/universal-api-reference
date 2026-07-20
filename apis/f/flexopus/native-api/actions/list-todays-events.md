# List Today's Events with Flexopus

Retrieves today's events from a Flexopus account.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/today`
- **Base URL:** `{tenantBaseUrl}/api/v1`
- **Official documentation:** [List Today's Events](https://flexopus.com/api/docs/#endpoints-GETapi-v1-events-today)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `building_id` | query | `number` | no | Identifier of the building to show events for. |
| `location_id` | query | `number` | no | Identifier of the location to show events for. |
| `bookable_id` | query | `number` | no | Identifier of the bookable to show events for. |
