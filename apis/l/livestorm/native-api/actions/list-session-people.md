# List Session People with Livestorm

Retrieves people for a session from Livestorm.

## Endpoint

- **Method:** `GET`
- **Path:** `sessions/:id/people`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [List Session People](https://developers.livestorm.co/reference/get_sessions-id-people)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Session ID |
| `filter[role]` | query | `string` | no | Filter People by role : 'participant', 'team_member' |
| `filter[attended]` | query | `boolean` | no | Filter People that attend or not the Session |
| `filter[email]` | query | `string` | no | Filter People by their email (exact match) |
| `filter[created_since]` | query | `date` | no | Filter People which ‘created_at’ attribute starts from the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[created_until]` | query | `date` | no | Filter People which ‘created_at’ attribute ends with the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[updated_since]` | query | `date` | no | Filter People which ‘updated_at’ attribute starts from the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[updated_until]` | query | `date` | no | Filter People which ‘updated_at’ attribute ends with the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `include` | query | `string` | no | Include Related Data Send multiple values as a string separated by `,`. |
