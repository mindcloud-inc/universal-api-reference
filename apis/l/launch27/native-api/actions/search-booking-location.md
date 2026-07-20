# Search Booking Location with Launch27

Finds a booking location in Launch27.

## Endpoint

- **Method:** `POST`
- **Path:** `booking/location`
- **Base URL:** `https://{subdomain}.launch27.com/v1`
- **Official documentation:** [Search Booking Location](https://api.launch27.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | yes | Street address to search against Launch27 booking locations. |
| `zip` | body | `string` | yes | Postal code for the booking location search. |
| `city` | body | `string` | no | City for the booking location search. |
| `state` | body | `string` | no | State or region for the booking location search. |
