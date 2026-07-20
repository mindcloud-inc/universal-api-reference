# Update Ad with Reddit Lead Ads

Updates an ad in Reddit Ads.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/ads/{ad_id}`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [Update Ad](https://ads-api.reddit.com/docs/v3/operations/update-ad)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ad_id` | path | `string` | yes | Reddit Ads ad identifier. |
| `data` | body | `object` | yes | JSON request body from the Reddit Ads API spec. |
