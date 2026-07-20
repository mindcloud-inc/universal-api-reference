# List Teams with Timetoreply

## Endpoint

- **Method:** `GET`
- **Path:** `/api/entities/teams`
- **Base URL:** `https://portal.timetoreply.com`
- **Official documentation:** [List Teams](https://portal.timetoreply.com/api-docs#entities-GETapi-entities-teams)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_emails` | query | `boolean` | no | Include team email addresses in the response. |
| `search` | query | `string` | no | Filter teams by a search term. |
