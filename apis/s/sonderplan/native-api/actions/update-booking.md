# Update Booking with Sonderplan

## Endpoint

- **Method:** `PUT`
- **Path:** `/booking`
- **Base URL:** `https://api.sonderplan.com/v2`
- **Official documentation:** [Update Booking](https://docs.sonderplan.com/api-reference/booking/update-booking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Booking payload. |
| `id` | query | `string` | yes | Booking ID. |
