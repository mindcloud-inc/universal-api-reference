# Get attached EventDates of Ticket Type with Eventix

Retrieves event dates for an Eventix ticket type.

## Endpoint

- **Method:** `GET`
- **Path:** `/3.0.0/ticket/:guid/dates`
- **Base URL:** `https://api.weeztix.com`
- **Official documentation:** [Get attached EventDates of Ticket Type](https://docs.weeztix.com/api/dashboard/get-ticket-specific-event-dates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guid` | path | `string` | yes | The guid of the Ticket Type. |
