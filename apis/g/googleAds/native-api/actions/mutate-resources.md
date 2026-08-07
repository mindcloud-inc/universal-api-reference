# Mutate Resources with Google Ads

Creates, updates, or removes resources in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/googleAds:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Mutate Resources](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Mutate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | no | — |
| `mutateOperations[]` | body | `array<object>` | no | Required. The list of operations to perform on individual resources. |
| `partialFailure` | body | `boolean` | no | If true, successful operations will be carried out and invalid operations will return errors. If false, all operations will be carried out in one transaction if and only if they are all valid. Default is false. Format: `toggle`. |
| `validateOnly` | body | `boolean` | no | If true, the request is validated but not executed. Only errors are returned, not results. Format: `toggle`. |
| `responseContentType` | body | `list` | no | The response content type setting. Determines whether the mutable resource or just the resource name should be returned post mutation. The mutable resource will only be returned if the resource has the appropriate response field. For example, MutateCampaignResult.campaign. |
