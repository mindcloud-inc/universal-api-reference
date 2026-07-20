# List Teams with Runrun.it

Retrieves teams from Runrun.it.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [List Teams](https://runrun.it/api/documentation#teams-list-teams)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sort` | query | `string` | no | Sort by column |
| `sort_dir` | query | `string` | no | Sort direction ('asc' or 'desc') |
| `search_term` | query | `string` | no | Filter by term |
| `filter_id` | query | `number` | no | Filter by an existing filter |
