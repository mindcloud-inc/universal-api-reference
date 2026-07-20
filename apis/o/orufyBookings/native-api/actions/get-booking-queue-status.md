# Get Booking Queue Status with Orufy Bookings

## Endpoint

- **Method:** `GET`
- **Path:** `/meet/queue-event/status/:queueId`
- **Base URL:** `https://bookings.orufy.com/api/v1/bookings`
- **Official documentation:** [Get Booking Queue Status](https://orufy.com/support/bookings/eventtype/bookinginfo)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queueId` | path | `string` | yes | The queue identifier returned by Create Booking. |
