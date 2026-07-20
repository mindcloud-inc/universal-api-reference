# Update Ad Group with Reddit Lead Ads

Updates an ad group in Reddit Ads.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/ad_groups/{ad_group_id}`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [Update Ad Group](https://ads-api.reddit.com/docs/v3/operations/update-ad-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ad_group_id` | path | `string` | yes | Reddit Ads ad group identifier. |
| `data` | body | `object` | yes | JSON request body from the Reddit Ads API spec. |
