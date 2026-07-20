# List People with RO App

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/people`
- **Base URL:** `https://api.roapp.io/v2`
- **Official documentation:** [List People](https://roapp.readme.io/reference/get-list-of-people)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number |
| `names[]` | query | `array<string>` | no | List of names |
| `phones[]` | query | `array<string>` | no | List of phones |
| `managers[]` | query | `array<number>` | no | List of Employee IDs |
| `created_at[]` | query | `array<date>` | no | Filter by creation date. Accepts an array with one or two ISO 8601 date-time values. If one value is provided, it represents the start (left) boundary. If two values are provided, they define a date range (start and end). Examples: ["2025-05-01T00:00:00Z"] — filter from May 1, 2025 onward. ["2025-05-01T00:00:00Z", "2025-05-02T00:00:00Z"] — filter between May 1 and May 2, 2025. |
| `modified_at[]` | query | `array<date>` | no | Filter by modification date. Accepts an array with one or two ISO 8601 date-time values. If one value is provided, it represents the start (left) boundary. If two values are provided, they define a date range (start and end). Examples: ["2025-05-01T00:00:00Z"] — filter from May 1, 2025 onward. ["2025-05-01T00:00:00Z", "2025-05-02T00:00:00Z"] — filter between May 1 and May 2, 2025. |
| `sort` | query | `string` | no | Defines the sorting order of returned results. Use a field name to sort ascending or prefix it with a minus sign (-) to sort descending. |
