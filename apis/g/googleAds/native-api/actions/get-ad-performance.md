# Get Ad Performance with Google Ads

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/googleAds:search`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [Get Ad Performance](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list<string>` | yes | Customer ID to query (without dashes). |
| `startDate` | body | `string` | no | Start date for the reporting window (YYYY-MM-DD). |
| `endDate` | body | `string` | no | End date for the reporting window (YYYY-MM-DD). |
