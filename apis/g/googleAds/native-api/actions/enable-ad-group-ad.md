# Enable Ad Group Ad with Google Ads

Updates an ad group ad to enabled status in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/adGroupAds:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Enable Ad Group Ad](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupAdService/MutateAdGroupAds)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | — |
| `operations[]` | body | `array<object>` | yes | List of mutate operations. |
| `operations[].update` | body | `object` | no | Update payload for each mutate operation. |
| `operations[].update.resourceName` | body | `string` | yes | — |
| `partialFailure` | body | `boolean` | no | — |
| `responseContentType` | body | `list` | no | Accepted values: `MUTABLE_RESOURCE`, `RESOURCE_NAME_ONLY`, `UNSPECIFIED`. |
| `validateOnly` | body | `boolean` | no | — |
