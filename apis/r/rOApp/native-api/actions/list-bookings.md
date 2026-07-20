# List Bookings with RO App

## Endpoint

- **Method:** `GET`
- **Path:** `/bookings`
- **Base URL:** `https://api.roapp.io/v2`
- **Official documentation:** [List Bookings](https://roapp.readme.io/reference/get-bookigs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number |
| `branches[]` | query | `array<number>` | no | List of Location IDs |
| `ids[]` | query | `array<number>` | no | List of Booking IDs |
| `statuses[]` | query | `array<number>` | no | Array of Booking status IDs |
| `assignees[]` | query | `array<number>` | no | Array of employee IDs |
| `clients_ids[]` | query | `array<number>` | no | List of client (person / organization) IDs |
| `client_names[]` | query | `array<string>` | no | List of client (person / organization) names |
| `client_phones[]` | query | `array<string>` | no | List of phone numbers |
| `created_at[]` | query | `array<date>` | no | Filter by creation date. Accepts an array with one or two ISO 8601 date-time values. If one value is provided, it represents the start (left) boundary. If two values are provided, they define a date range (start and end). Examples: ["2025-05-01T00:00:00Z"] — filter from May 1, 2025 onward. ["2025-05-01T00:00:00Z", "2025-05-02T00:00:00Z"] — filter between May 1 and May 2, 2025. |
| `modified_at[]` | query | `array<date>` | no | Filter by modification date. Accepts an array with one or two ISO 8601 date-time values. If one value is provided, it represents the start (left) boundary. If two values are provided, they define a date range (start and end). Examples: ["2025-05-01T00:00:00Z"] — filter from May 1, 2025 onward. ["2025-05-01T00:00:00Z", "2025-05-02T00:00:00Z"] — filter between May 1 and May 2, 2025. |
| `scheduled_for[]` | query | `array<date>` | no | Filter by "Scheduled from" date and time. Accepts an array with one or two ISO 8601 date-time values. If one value is provided, it represents the start (left) boundary. If two values are provided, they define a date range (start and end). Examples: ["2025-05-01T00:00:00Z"] — filter from May 1, 2025 onward. ["2025-05-01T00:00:00Z", "2025-05-02T00:00:00Z"] — filter between May 1 and May 2, 2025. |
| `sort` | query | `string` | no | Defines the sorting order of returned results. Use a field name to sort ascending or prefix it with a minus sign (-) to sort descending. |
