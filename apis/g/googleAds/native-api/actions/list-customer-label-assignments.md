# List Customer Label Assignments with Google Ads

Retrieves customer label assignments from Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/googleAds:search`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [List Customer Label Assignments](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list<string>` | yes | Customer ID to query (without dashes). |
| `query` | body | `string` | yes | GAQL query for customer_label assignments. |
