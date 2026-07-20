# List Events with Understory

Retrieves events from Understory.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/events`
- **Base URL:** `https://api.understory.io`
- **Official documentation:** [List Events](https://developer.understory.io/apis/event/getevents.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `date` | no | Filter events starting from this local date-time. |
| `to` | query | `date` | no | Filter events up to this local date-time. |
