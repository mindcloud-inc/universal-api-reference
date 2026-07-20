# Get Public Event with Orufy Bookings

## Endpoint

- **Method:** `GET`
- **Path:** `/website/event/:accessLink/:slug`
- **Base URL:** `https://bookings.orufy.com/api/v1/bookings`
- **Official documentation:** [Get Public Event](https://orufy.com/bookings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accessLink` | path | `string` | yes | The Orufy access link, for example `mindcloud`. |
| `slug` | path | `string` | yes | The public event slug, for example `30-min-intro-call`. |
