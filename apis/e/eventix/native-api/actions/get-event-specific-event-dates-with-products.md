# Get EventDates for Event with Products with Eventix

Retrieves event dates with products for an Eventix event.

## Endpoint

- **Method:** `GET`
- **Path:** `/3.0.0/event/:guid/dates/products`
- **Base URL:** `https://api.weeztix.com`
- **Official documentation:** [Get EventDates for Event with Products](https://docs.weeztix.com/api/dashboard/get-event-specific-event-dates-with-products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guid` | path | `string` | yes | The guid of the Event. |
