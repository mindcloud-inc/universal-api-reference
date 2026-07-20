# Search Communities with Reddit Lead Ads

Finds targetable communities in Reddit Ads by name or topic.

## Endpoint

- **Method:** `GET`
- **Path:** `/targeting/communities/search`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [Search Communities](https://ads-api.reddit.com/docs/v3/operations/search-communities)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Community search text. |
