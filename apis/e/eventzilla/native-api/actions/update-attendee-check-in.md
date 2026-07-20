# Update Attendee Check-In with Eventzilla

Updates attendee check-in status in Eventzilla.

## Endpoint

- **Method:** `POST`
- **Path:** `/attendees/checkin`
- **Base URL:** `https://www.eventzillaapi.net/api/v2`
- **Official documentation:** [Update Attendee Check-In](https://developer.eventzilla.net/docs/#att_checkin)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `barcode` | body | `string` | yes |
| `eventcheckin` | body | `boolean` | yes |
