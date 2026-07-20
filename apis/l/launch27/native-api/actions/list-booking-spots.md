# List Booking Spots with Launch27

Retrieves available booking spots from Launch27.

## Endpoint

- **Method:** `POST`
- **Path:** `booking/spots`
- **Base URL:** `https://{subdomain}.launch27.com/v1`
- **Official documentation:** [List Booking Spots](https://api.launch27.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | body | `string` | yes | Start date for booking spot availability in YYYY-MM-DD format. |
| `location_id` | body | `number` | yes | Launch27 location ID to search for available spots. |
| `duration` | body | `number` | yes | Requested service duration in minutes. |
