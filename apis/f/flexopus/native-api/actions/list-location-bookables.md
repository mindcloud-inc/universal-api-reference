# List Location Bookables with Flexopus

Retrieves bookables for a specific Flexopus location.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations/:location_id/bookables`
- **Base URL:** `{tenantBaseUrl}/api/v1`
- **Official documentation:** [List Location Bookables](https://flexopus.com/api/docs/#endpoints-GETapi-v1-locations--location_id--bookables)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location_id` | path | `number` | yes | The ID of the location. |
