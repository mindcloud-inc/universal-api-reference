# Create Booking with Orufy Bookings

## Endpoint

- **Method:** `POST`
- **Path:** `/meet/book`
- **Base URL:** `https://bookings.orufy.com/api/v1/bookings`
- **Official documentation:** [Create Booking](https://orufy.com/support/bookings/eventtype/bookinginfo)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accessLink` | body | `string` | yes | The Orufy access link, for example `mindcloud`. |
| `slug` | body | `string` | yes | The public event slug, for example `30-min-intro-call`. |
| `timezone` | body | `string` | yes | An IANA timezone, for example `America/Sao_Paulo`. |
| `time[]` | body | `array<object>` | yes | An array of time objects. Each item must include a `time` ISO datetime value. |
| `answers[]` | body | `array<object>` | yes | An array of booking answers. Each item should include `name` and `answer`. |
