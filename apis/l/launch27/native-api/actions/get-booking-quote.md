# Get Booking Quote with Launch27

Retrieves a booking quote from Launch27.

## Endpoint

- **Method:** `POST`
- **Path:** `booking/quote`
- **Base URL:** `https://{subdomain}.launch27.com/v1`
- **Official documentation:** [Get Booking Quote](https://api.launch27.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `quote_uuid` | body | `string` | yes | Launch27 quote UUID used to retrieve a booking quote. |
