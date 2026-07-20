# Update Campaign with Reddit Lead Ads

Updates a campaign in Reddit Ads.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/campaigns/{campaign_id}`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [Update Campaign](https://ads-api.reddit.com/docs/v3/operations/update-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | Reddit Ads campaign identifier. |
| `data` | body | `object` | yes | JSON request body from the Reddit Ads API spec. |
