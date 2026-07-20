# Get Locations with Eventix

Retrieves locations from Eventix.

## Endpoint

- **Method:** `GET`
- **Path:** `/3.0.0/location/:type`
- **Base URL:** `https://api.weeztix.com`
- **Official documentation:** [Get Locations](https://docs.weeztix.com/api/dashboard/get-event-locations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `list<string>` | yes | How to handle archived Locations. Accepted values: `0`, `1`, `2`. |
