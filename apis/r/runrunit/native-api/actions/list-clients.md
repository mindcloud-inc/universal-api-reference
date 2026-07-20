# List Clients with Runrun.it

Retrieves clients from Runrun.it.

## Endpoint

- **Method:** `GET`
- **Path:** `/clients`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [List Clients](https://runrun.it/api/documentation#clients-list-clients)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sort` | query | `string` | no | Sort by column |
| `sort_dir` | query | `string` | no | Sort direction ('asc' or 'desc') |
| `search_term` | query | `string` | no | Filter by term |
| `filter_id` | query | `number` | no | Filter by an existing filter |
| `is_visible` | query | `boolean` | no | Filter by visible clients |
