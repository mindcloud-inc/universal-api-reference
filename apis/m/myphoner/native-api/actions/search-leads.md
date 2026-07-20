# Search Leads with Myphoner

Searches for leads in Myphoner by query.

## Endpoint

- **Method:** `GET`
- **Path:** `/leads/search`
- **Base URL:** `https://{subdomain}.myphoner.com/api/v2`
- **Official documentation:** [Search Leads](https://www.myphoner.com/docs/api/#leads)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_ids` | query | `string` | no | Comma-separated list IDs to scope the search to specific lists. |
| `query` | query | `string` | yes | Free-text search query across lead data and activity logs. |
