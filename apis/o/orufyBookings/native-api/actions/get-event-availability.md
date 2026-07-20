# Get Event Availability with Orufy Bookings

## Endpoint

- **Method:** `POST`
- **Path:** `/website/dates`
- **Base URL:** `https://bookings.orufy.com/api/v1/bookings`
- **Official documentation:** [Get Event Availability](https://orufy.com/support/bookings/firstsetup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accessLink` | body | `string` | yes | The Orufy access link, for example `mindcloud`. |
| `slug` | body | `string` | yes | The public event slug, for example `30-min-intro-call`. |
| `timezone` | body | `string` | yes | An IANA timezone, for example `America/Sao_Paulo`. |
| `start` | body | `date` | yes | The start date to check availability for, in ISO format. |
| `end` | body | `date` | yes | The end date to check availability for, in ISO format. |
