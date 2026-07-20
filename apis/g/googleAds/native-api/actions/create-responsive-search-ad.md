# Create Responsive Search Ad with Google Ads

Creates a responsive search ad in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/adGroupAds:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [Create Responsive Search Ad](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupAdService/MutateAdGroupAds)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | — |
| `partialFailure` | body | `boolean` | no | — |
| `validateOnly` | body | `boolean` | no | — |
| `operations[]` | body | `array<object>` | yes | Mutate operations to apply for ad group ads. |
| `operations[].create` | body | `object` | no | Ad group ad creation payload. |
| `operations[].create.ad` | body | `object` | no | Ad content payload. |
| `operations[].create.ad.responsiveSearchAd` | body | `object` | no | Responsive search ad fields. |
| `responseContentType` | body | `list` | no | Accepted values: `MUTABLE_RESOURCE`, `RESOURCE_NAME_ONLY`, `UNSPECIFIED`. |
| `operations[].create.status` | body | `list` | no | Accepted values: `ENABLED`, `PAUSED`, `REMOVED`, `UNKNOWN`, `UNSPECIFIED`. |
| `operations[].create.adGroup` | body | `string` | yes | — |
| `operations[].create.ad.finalUrls[]` | body | `array<string>` | yes | — |
| `operations[].create.ad.responsiveSearchAd.headlines[]` | body | `array<object>` | yes | Headline assets for the responsive search ad (array of objects with text). |
| `operations[].create.ad.responsiveSearchAd.descriptions[]` | body | `array<object>` | yes | Description assets for the responsive search ad (array of objects with text). |
