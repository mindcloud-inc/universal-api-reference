# Get EventDates for specific Location with Eventix

Retrieves event dates for an Eventix location.

## Endpoint

- **Method:** `GET`
- **Path:** `/3.0.0/location/:guid/dates`
- **Base URL:** `https://api.weeztix.com`
- **Official documentation:** [Get EventDates for specific Location](https://docs.weeztix.com/api/dashboard/get-event-location-specific-event-dates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guid` | path | `string` | yes | The guid of the Location. |
