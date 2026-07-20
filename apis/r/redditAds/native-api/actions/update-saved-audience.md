# Update Saved Audience with Reddit Lead Ads

Updates a saved audience in Reddit Ads.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/saved_audiences/{saved_audience_id}`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [Update Saved Audience](https://ads-api.reddit.com/docs/v3/operations/update-saved-audience)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `saved_audience_id` | path | `string` | yes | Reddit Ads saved audience identifier. |
| `data` | body | `object` | yes | JSON request body from the Reddit Ads API spec. |
