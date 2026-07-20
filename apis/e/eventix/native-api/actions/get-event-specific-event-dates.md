# Get EventDates for Event with Eventix

Retrieves event dates for an Eventix event.

## Endpoint

- **Method:** `GET`
- **Path:** `/3.0.0/event/:guid/dates`
- **Base URL:** `https://api.weeztix.com`
- **Official documentation:** [Get EventDates for Event](https://docs.weeztix.com/api/dashboard/get-event-specific-event-dates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guid` | path | `string` | yes | The guid of the Event. |
