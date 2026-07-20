# Retrieve the Event of an EventDate with Eventix

Retrieves the parent event of an Eventix event date.

## Endpoint

- **Method:** `GET`
- **Path:** `/3.0.0/eventdate/:guid/event`
- **Base URL:** `https://api.weeztix.com`
- **Official documentation:** [Retrieve the Event of an EventDate](https://docs.weeztix.com/api/dashboard/get-event-date-specific-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guid` | path | `string` | yes | The guid of the EventDate. |
