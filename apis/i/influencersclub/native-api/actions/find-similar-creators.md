# Find Similar Creators with Influencers.club

Finds creators similar to a reference creator in Influencers.club.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/discovery/creators/similar/`
- **Base URL:** `https://api-dashboard.influencers.club`
- **Official documentation:** [Find Similar Creators](https://docs.influencers.club/openapi/similar-creators/public_v1_discovery_creators_similar_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter_key` | body | `string` | yes | Field key to match for similar creators. |
| `filter_value` | body | `string` | yes | Field value to match for similar creators. |
| `paging.limit` | body | `number` | yes | Page size for similar creators response. |
| `paging.page` | body | `number` | yes | 0-indexed page number. |
