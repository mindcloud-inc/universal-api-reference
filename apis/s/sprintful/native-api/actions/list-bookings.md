# List Bookings with Sprintful

Retrieves booking events available in Sprintful.

## Endpoint

- **Method:** `GET`
- **Path:** `/bookings`
- **Base URL:** `https://app.sprintful.com/api/v1`
- **Official documentation:** [List Bookings](https://support.sprintful.com/article/129-sprintful-for-developers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | Maximum number of bookings to return. Sprintful defaults to 50. |
| `offset` | query | `string` | no | Number of bookings to skip before returning results. |
| `start_date` | query | `string` | no | Filter bookings starting on or after this date. Sprintful format: DD-MM-YYY. |
| `end_date` | query | `string` | no | Filter bookings ending on or before this date. Sprintful format: DD-MM-YYY. |
| `page_slug` | query | `string` | no | Only return bookings for a specific page slug. |
| `exclude_page_slug` | query | `string` | no | Exclude bookings for a specific page slug. |
