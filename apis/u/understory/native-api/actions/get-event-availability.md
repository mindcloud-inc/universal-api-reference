# Get Event Availability with Understory

Retrieves event availability from Understory.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/event-availabilities/{{eventId}}`
- **Base URL:** `https://api.understory.io`
- **Official documentation:** [Get Event Availability](https://developer.understory.io/apis/event-availability/geteventavailability.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The unique identifier of the event. |
