# List My Businesses with Reddit Lead Ads

Retrieves businesses for the authenticated user from Reddit Ads.

## Endpoint

- **Method:** `GET`
- **Path:** `/me/businesses`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [List My Businesses](https://ads-api.reddit.com/docs/v3/operations/list-my-businesses)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ad_account_id` | query | `string` | no | Optional ad account ID filter. |
| `role` | query | `string` | no | Optional business role filter. |
