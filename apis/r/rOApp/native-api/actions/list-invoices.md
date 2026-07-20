# List Invoices with RO App

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices`
- **Base URL:** `https://api.roapp.io/v2`
- **Official documentation:** [List Invoices](https://roapp.readme.io/reference/get-invoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number |
| `legal_entity_id` | query | `number` | no | Legal entity ID |
| `ids[]` | query | `array<number>` | no | List of Invoice IDs |
| `numbers[]` | query | `array<string>` | no | List of Invoice document numbers |
| `payment_method` | query | `string` | no | Invoice payment method |
| `statuses[]` | query | `array<number>` | no | List of Invoice status IDs |
| `client_ids[]` | query | `array<number>` | no | List of Client (Person / Organization) IDs |
| `payer_ids[]` | query | `array<number>` | no | List of Payer IDs |
| `managers[]` | query | `array<number>` | no | List of Manager IDs |
| `created_at[]` | query | `array<date>` | no | Filter by creation date. Accepts an array with one or two ISO 8601 date-time values. If one value is provided, it represents the start (left) boundary. If two values are provided, they define a date range (start and end). Examples: ["2025-05-01T00:00:00Z"] — filter from May 1, 2025 onward. ["2025-05-01T00:00:00Z", "2025-05-02T00:00:00Z"] — filter between May 1 and May 2, 2025. |
| `modified_at[]` | query | `array<date>` | no | Filter by modification date. Accepts an array with one or two ISO 8601 date-time values. If one value is provided, it represents the start (left) boundary. If two values are provided, they define a date range (start and end). Examples: ["2025-05-01T00:00:00Z"] — filter from May 1, 2025 onward. ["2025-05-01T00:00:00Z", "2025-05-02T00:00:00Z"] — filter between May 1 and May 2, 2025. |
| `issue_date[]` | query | `array<date>` | no | Filter by date of issue. Accepts an array with one or two ISO 8601 date-time values. If one value is provided, it represents the start (left) boundary. If two values are provided, they define a date range (start and end). Examples: ["2025-05-01T00:00:00Z"] — filter from May 1, 2025 onward. ["2025-05-01T00:00:00Z", "2025-05-02T00:00:00Z"] — filter between May 1 and May 2, 2025. |
| `due_date[]` | query | `array<date>` | no | Filter by due date. Accepts an array with one or two ISO 8601 date-time values. If one value is provided, it represents the start (left) boundary. If two values are provided, they define a date range (start and end). Examples: ["2025-05-01T00:00:00Z"] — filter from May 1, 2025 onward. ["2025-05-01T00:00:00Z", "2025-05-02T00:00:00Z"] — filter between May 1 and May 2, 2025. |
| `sort` | query | `string` | no | Defines the sorting order of returned results. Use a field name to sort ascending or prefix it with a minus sign (-) to sort descending. |
