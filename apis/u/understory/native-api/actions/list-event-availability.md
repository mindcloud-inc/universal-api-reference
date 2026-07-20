# List Event Availability with Understory

Retrieves event availability for an experience in Understory.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/event-availabilities`
- **Base URL:** `https://api.understory.io`
- **Official documentation:** [List Event Availability](https://developer.understory.io/apis/event-availability/listeventavailability.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `experienceId` | query | `string` | yes | The unique identifier of the experience to query events for. |
| `from` | query | `date` | no | Filter events starting from this local date-time. |
| `to` | query | `date` | no | Filter events up to this local date-time. |
