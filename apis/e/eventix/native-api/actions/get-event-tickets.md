# Get Ticket Types for Event with Eventix

Retrieves ticket types for an Eventix event.

## Endpoint

- **Method:** `GET`
- **Path:** `/3.0.0/event/:guid/ticket/:type`
- **Base URL:** `https://api.weeztix.com`
- **Official documentation:** [Get Ticket Types for Event](https://docs.weeztix.com/api/dashboard/get-event-tickets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guid` | path | `string` | yes | The guid of the Event. |
| `type` | path | `list<string>` | yes | How to handle archived Ticket Types for the event. Accepted values: `0`, `1`, `2`. |
