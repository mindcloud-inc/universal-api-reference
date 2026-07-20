# Search Creators (Discovery) with Influencers.club

Finds creators in Influencers.club by platform-specific discovery filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/discovery/`
- **Base URL:** `https://api-dashboard.influencers.club`
- **Official documentation:** [Search Creators (Discovery)](https://docs.influencers.club/openapi/discovery-api/public_v1_discovery_create)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `platform` | body | `string` | yes | Creator platform to query (e.g., instagram). |
| `paging.limit` | body | `number` | yes | Page size for discovery results. |
| `paging.page` | body | `number` | yes | 0-indexed page number. |
| `filters.ai_search` | body | `string` | yes | Natural-language discovery query. |
| `sort.sort_by` | body | `string` | no | Field used for sorting. |
| `sort.sort_order` | body | `string` | no | Sort direction (asc or desc). |
| `filters.is_verified` | body | `boolean` | no | Only include verified creators when true. |
| `filters.number_of_followers.min` | body | `number` | no | Minimum follower count filter. |
| `filters.number_of_followers.max` | body | `number` | no | Maximum follower count filter. |
