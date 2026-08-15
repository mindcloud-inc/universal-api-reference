# Remove Ad Group Ad with Google Ads

Deletes an ad group ad from Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/adGroupAds:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Remove Ad Group Ad](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupAdService/MutateAdGroupAds)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | — |
| `operations[]` | body | `array<object>` | yes | List of mutate operations. |
| `operations[].remove` | body | `string` | yes | — |
| `partialFailure` | body | `boolean` | no | — |
| `responseContentType` | body | `list` | no | Accepted values: `MUTABLE_RESOURCE`, `RESOURCE_NAME_ONLY`, `UNSPECIFIED`. |
| `validateOnly` | body | `boolean` | no | — |
