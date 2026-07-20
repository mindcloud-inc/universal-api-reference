# Get Scanning stats for an event with Eventix

Retrieves scanning stats for an Eventix event.

## Endpoint

- **Method:** `GET`
- **Path:** `/3.0.0/event/:guid/scanningstats`
- **Base URL:** `https://api.weeztix.com`
- **Official documentation:** [Get Scanning stats for an event](https://docs.weeztix.com/api/dashboard/get-event-specific-scanning-stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guid` | path | `string` | yes | The guid of the Event. |
