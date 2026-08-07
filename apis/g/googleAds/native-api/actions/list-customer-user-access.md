# List Customer User Access with Google Ads

Retrieves customer user access from Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/googleAds:search`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [List Customer User Access](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list<string>` | yes | Customer ID to query (without dashes). |
| `query` | body | `string` | yes | GAQL query for customer_user_access visibility. |
