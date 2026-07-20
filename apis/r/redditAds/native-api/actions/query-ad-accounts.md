# Query Ad Accounts with Reddit Lead Ads

Finds ad accounts for a business in Reddit Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `/businesses/{business_id}/ad_accounts/query`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [Query Ad Accounts](https://ads-api.reddit.com/docs/v3/operations/query-ad-accounts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | path | `string` | yes | The ID of the business to list ad accounts for. |
| `data` | body | `object` | yes | JSON request body from the Reddit Ads API spec. |
