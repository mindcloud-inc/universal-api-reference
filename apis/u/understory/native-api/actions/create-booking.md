# Create Booking with Understory

Creates a new booking in Understory.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/bookings`
- **Base URL:** `https://api.understory.io`
- **Official documentation:** [Create Booking](https://developer.understory.io/apis/booking/createbooking.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_id` | body | `string` | yes | The unique identifier of the event. |
| `customer` | body | `object` | yes | The customer making the booking as a structured object. |
| `locale` | body | `string` | yes | A lowercase ISO 639-1 language code, optionally with country suffix like en-US. |
| `items` | body | `list<object>` | yes | One or more booking items as a list of objects. |
| `metadata` | body | `object` | no | Optional custom metadata object for the booking. |
