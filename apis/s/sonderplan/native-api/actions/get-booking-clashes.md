# Get Booking Clashes with Sonderplan

## Endpoint

- **Method:** `GET`
- **Path:** `/booking/checkclash`
- **Base URL:** `https://api.sonderplan.com/v2`
- **Official documentation:** [Get Booking Clashes](https://docs.sonderplan.com/api-reference/booking/get-booking-clashes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | query | `string` | yes | End datetime for clash checking. |
| `start` | query | `string` | yes | Start datetime for clash checking. |
