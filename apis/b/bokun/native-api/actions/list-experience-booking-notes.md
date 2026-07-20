# List Experience Booking Notes with Bokun

Retrieves notes for an experience booking from Bokun.

## Endpoint

- **Method:** `GET`
- **Path:** `/restapi/v2.0/experienceBooking/:experienceBookingId/notes`
- **Base URL:** `https://api.bokun.io`
- **Official documentation:** [List Experience Booking Notes](https://api-docs.bokun.dev/rest-v2.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `experienceBookingId` | path | `number` | yes | The Bokun experience booking ID. |
