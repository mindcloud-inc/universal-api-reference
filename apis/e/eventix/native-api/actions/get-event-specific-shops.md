# Get all Shops of an Event with Eventix

Retrieves shops for an Eventix event.

## Endpoint

- **Method:** `GET`
- **Path:** `/3.0.0/event/:guid/shops`
- **Base URL:** `https://api.weeztix.com`
- **Official documentation:** [Get all Shops of an Event](https://docs.weeztix.com/api/dashboard/get-event-specific-shops)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guid` | path | `string` | yes | The guid of the Event. |
