# List Pixels By Business with Reddit Lead Ads

Retrieves pixels for a business from Reddit Ads.

## Endpoint

- **Method:** `GET`
- **Path:** `/businesses/{business_id}/pixels`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [List Pixels By Business](https://ads-api.reddit.com/docs/v3/operations/list-pixels-by-business)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | path | `string` | yes | The ID of the business to list pixels for. |
