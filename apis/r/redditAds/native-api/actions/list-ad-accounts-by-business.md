# List Ad Accounts By Business with Reddit Lead Ads

Retrieves ad accounts for a business from Reddit Ads.

## Endpoint

- **Method:** `GET`
- **Path:** `/businesses/{business_id}/ad_accounts`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [List Ad Accounts By Business](https://ads-api.reddit.com/docs/v3/operations/list-ad-accounts-by-business)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | path | `string` | yes | The ID of the business to get ad accounts for. |
| `ids` | query | `string` | no | Optional ad account IDs filter. |
