# List Events with Livestorm

Retrieves events from Livestorm.

## Endpoint

- **Method:** `GET`
- **Path:** `events`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [List Events](https://developers.livestorm.co/reference/get_events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[title]` | query | `string` | no | Filter Events by title |
| `filter[everyone_can_speak]` | query | `string` | no | Filter Events by everyone_can_speak |
| `filter[scheduling_status]` | query | `string` | no | Filter Events by scheduling_status                       (live, upcoming, on_demand, ended, not_started, draft, cancelled, not_scheduled) |
| `filter[created_since]` | query | `date` | no | Filter Events which ‘created_at’ attribute starts from the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[created_until]` | query | `date` | no | Filter Events which ‘created_at’ attribute ends with the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[updated_since]` | query | `date` | no | Filter Events which ‘updated_at’ attribute starts from the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[updated_until]` | query | `date` | no | Filter Events which ‘updated_at’ attribute ends with the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[tag]` | query | `string` | no | Filter Events by tag title (case-insensitive, comma-separated for multiple tags) Send multiple values as a string separated by `,`. |
| `include` | query | `string` | no | Include Related Data Send multiple values as a string separated by `,`. |
