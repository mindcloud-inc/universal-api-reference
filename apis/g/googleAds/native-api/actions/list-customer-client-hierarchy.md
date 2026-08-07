# List Customer Client Hierarchy with Google Ads

Retrieves customer client hierarchy from Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/googleAds:search`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [List Customer Client Hierarchy](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list<string>` | yes | Customer ID to query (without dashes). |
| `query` | body | `string` | yes | GAQL query for customer_client hierarchy. |
