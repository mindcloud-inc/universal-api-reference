# Get Local Services Lead with Google Ads

Retrieves a local services lead from Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/googleAds:search`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Get Local Services Lead](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID that owns the Google Ads resources (without dashes). |
| `leadId` | body | `string` | no | Optional local services lead ID for convenience when composing a query. |
| `query` | body | `string` | yes | GAQL query to retrieve a specific local services lead. |
