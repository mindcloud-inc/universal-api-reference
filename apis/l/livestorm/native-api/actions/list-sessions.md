# List Sessions with Livestorm

Retrieves sessions from Livestorm.

## Endpoint

- **Method:** `GET`
- **Path:** `sessions`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [List Sessions](https://developers.livestorm.co/reference/get_sessions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[status]` | query | `string` | no | Filter Sessions by status : 'upcoming', 'live', 'on_demand', 'past', 'past_not_started', 'canceled', 'draft' |
| `filter[date_from]` | query | `date` | no | Filter Sessions which ‘estimated_started_at’ attribute starts from the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[date_to]` | query | `date` | no | Filter Sessions which ‘estimated_started_at’ attribute ends with the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[created_since]` | query | `date` | no | Filter Sessions which ‘created_at’ attribute starts from the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[created_until]` | query | `date` | no | Filter Sessions which ‘created_at’ attribute ends with the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[updated_since]` | query | `date` | no | Filter Sessions which ‘updated_at’ attribute starts from the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[updated_until]` | query | `date` | no | Filter Sessions which ‘updated_at’ attribute ends with the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[include_breakout_rooms]` | query | `string` | no | Filter Sessions depending upon if they are breakout room sessions or not |
