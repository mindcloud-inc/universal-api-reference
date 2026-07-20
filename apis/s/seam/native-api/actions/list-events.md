# List Events with Seam

Retrieves a list of events from Seam.

## Endpoint

- **Method:** `POST`
- **Path:** `/events/list`
- **Base URL:** `https://connect.getseam.com`
- **Official documentation:** [List Events](https://docs.seam.co/latest/api/events/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connected_account_id` | body | `string` | no | ID of the connected account for which you want to list events. |
| `device_id` | body | `string` | no | ID of the device for which you want to list events. |
| `event_type` | body | `string` | no | Type of events that you want to list. |
| `since` | body | `string` | yes | Beginning timestamp for the events that you want to list. This action currently requires `since` because `between` is not exposed yet. |
