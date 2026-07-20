# Get EventDates with Eventix

Retrieves event dates from Eventix.

## Endpoint

- **Method:** `GET`
- **Path:** `/3.0.0/eventdate/:type`
- **Base URL:** `https://api.weeztix.com`
- **Official documentation:** [Get EventDates](https://docs.weeztix.com/api/dashboard/get-event-dates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `list<string>` | yes | How to handle archived EventDates. Accepted values: `0`, `1`, `2`. |
