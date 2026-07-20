# Create Reservation with Starfish

Creates a new reservation in Starfish.

## Endpoint

- **Method:** `POST`
- **Path:** `/reservations`
- **Base URL:** `https://api.camping.care/v21`
- **Official documentation:** [Create Reservation](https://documenter.getpostman.com/view/9467805/VUjQkj1d)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accommodation_id` | body | `number` | yes | Accommodation ID. |
| `arrival` | body | `string` | yes | Reservation arrival date. |
| `departure` | body | `string` | yes | Reservation departure date. |
| `persons` | body | `number` | yes | Number of persons. |
| `last_name` | body | `string` | yes | Main traveler last name. |
| `email` | body | `string` | yes | Main traveler email. |
| `place_id` | body | `number` | no | Place ID. |
| `main_traveler` | body | `string` | no | Stringified JSON for the main traveler. |
| `force` | body | `string` | no | Force reservation creation. |
| `forced_rows` | body | `string` | no | Stringified JSON array of forced reservation rows. |
