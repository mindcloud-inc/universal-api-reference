# Update Custom Audience Users with Reddit Lead Ads

Updates users in a custom audience in Reddit Ads.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/custom_audiences/{audience_id}/users`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [Update Custom Audience Users](https://ads-api.reddit.com/docs/v3/operations/update-custom-audience-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience_id` | path | `string` | yes | Reddit Ads audience identifier. |
| `data` | body | `object` | yes | JSON request body from the Reddit Ads API spec. |
