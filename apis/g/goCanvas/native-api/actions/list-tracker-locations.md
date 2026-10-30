# List Tracker Locations with GoCanvas

## Endpoint

- **Method:** `GET`
- **Path:** `/tracker/locations`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [List Tracker Locations](https://api.gocanvas.com/api/v3/docs#list-all-locations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | yes | ISO 8601 date or datetime. A date alone means the start of that day. |
| `end_date` | query | `string` | yes | ISO 8601 date or datetime. A date alone means 23:59:59 on that day. |
| `user_id` | query | `number` | no | Limit results to this user; omit for all company users. |
| `use_created_at` | query | `boolean` | no | Filter and sort by upload time instead of recorded time when true. |
