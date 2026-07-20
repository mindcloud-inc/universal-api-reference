# List Event People with Livestorm

Retrieves people for an event from Livestorm.

## Endpoint

- **Method:** `GET`
- **Path:** `events/:id/people`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [List Event People](https://developers.livestorm.co/reference/get_events-id-people)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Event ID |
| `filter[role]` | query | `string` | no | Filter People by role : 'participant', 'team_member' |
| `filter[email]` | query | `string` | no | Filter People by their email (exact match) |
