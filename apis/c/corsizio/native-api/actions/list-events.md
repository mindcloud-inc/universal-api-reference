# List Events with Corsizio

Retrieves events from a Corsizio account.

## Endpoint

- **Method:** `GET`
- **Path:** `/events`
- **Base URL:** `https://api.corsizio.com/v1`
- **Official documentation:** [List Events](https://help.corsizio.com/article/39-api-get-events-list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order` | query | `list<string>` | no | Sort order such as startDate, endDate, created, or -endDate. Accepted values: `-created`, `-endDate`, `-startDate`, `created`, `endDate`, `startDate`. |
| `status` | query | `list<string>` | no | Event status filter such as published, draft, archived, deleted, or any. Accepted values: `any`, `archived`, `deleted`, `draft`, `published`. |
| `date` | query | `string` | no | Date range like 2026-03-01:2026-03-31. |
| `price` | query | `string` | no | Price range like 50:200 or :300. |
| `category` | query | `string` | no | Filter by a category ID from Corsizio account setup. |
| `location` | query | `string` | no | Filter by a location ID from Corsizio account setup. |
| `age` | query | `string` | no | Filter by an age group ID from Corsizio account setup. |
| `gender` | query | `string` | no | Filter by a gender ID from Corsizio account setup. |
| `level` | query | `string` | no | Filter by a level ID from Corsizio account setup. |
| `search` | query | `string` | no | Search by event name or exact event ID. |
| `include` | query | `list<string>` | no | Comma-separated values: details, filters, stats, config. Accepted values: `config`, `details`, `filters`, `stats`. Send multiple values as a string separated by `,`. |
| `expand` | query | `list<string>` | no | Comma-separated values: filters, instructors, account. Accepted values: `account`, `filters`, `instructors`. Send multiple values as a string separated by `,`. |
