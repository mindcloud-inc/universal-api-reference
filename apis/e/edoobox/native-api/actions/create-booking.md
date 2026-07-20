# Create Booking with Edoobox

Creates a new booking in Edoobox.

## Endpoint

- **Method:** `POST`
- **Path:** `/booking`
- **Base URL:** `https://app2.edoobox.com/v2`
- **Official documentation:** [Create Booking](https://api.docs.edoobox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | body | `string` | yes | edoobox user ID that owns the booking. |
| `offer` | body | `string` | yes | edoobox offer ID to book. |
| `waiting_list` | body | `boolean` | no | Whether to place the booking on the waiting list. |
