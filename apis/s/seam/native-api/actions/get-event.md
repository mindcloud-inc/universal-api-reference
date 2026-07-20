# Get Event with Seam

Retrieves an event from Seam.

## Endpoint

- **Method:** `POST`
- **Path:** `/events/get`
- **Base URL:** `https://connect.getseam.com`
- **Official documentation:** [Get Event](https://docs.seam.co/latest/api/events/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `device_id` | body | `string` | no | Unique identifier for the device that triggered the event that you want to get. |
| `event_id` | body | `string` | no | Unique identifier for the event that you want to get. |
| `event_type` | body | `string` | no | Type of the event that you want to get. |
