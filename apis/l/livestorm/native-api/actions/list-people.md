# List People with Livestorm

Retrieves people from Livestorm.

## Endpoint

- **Method:** `GET`
- **Path:** `people`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [List People](https://developers.livestorm.co/reference/get_people)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[role]` | query | `string` | no | Filter People by role : 'participant', 'team_member' |
| `filter[email]` | query | `string` | no | Filter People by their email (exact match) |
