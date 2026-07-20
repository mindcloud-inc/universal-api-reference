# List Event Sessions with Livestorm

Retrieves sessions for an event from Livestorm.

## Endpoint

- **Method:** `GET`
- **Path:** `events/:id/sessions`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [List Event Sessions](https://developers.livestorm.co/reference/get_events-id-sessions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Event ID |
| `filter[status]` | query | `string` | no | Filter Sessions by status : 'upcoming', 'live', 'on_demand', 'past', 'past_not_started', 'canceled', 'draft' |
| `filter[date_from]` | query | `date` | no | Filter Sessions which ‘estimated_started_at’ attribute starts from the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[date_to]` | query | `date` | no | Filter Sessions which ‘estimated_started_at’ attribute ends with the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[created_since]` | query | `date` | no | Filter Sessions which ‘created_at’ attribute starts from the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[created_until]` | query | `date` | no | Filter Sessions which ‘created_at’ attribute ends with the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[updated_since]` | query | `date` | no | Filter Sessions which ‘updated_at’ attribute starts from the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[updated_until]` | query | `date` | no | Filter Sessions which ‘updated_at’ attribute ends with the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[include_breakout_rooms]` | query | `string` | no | Filter Sessions depending upon if they are breakout room sessions or not |
| `include` | query | `string` | no | Include Related Data Send multiple values as a string separated by `,`. |
