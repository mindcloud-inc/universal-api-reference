# Upload Conversion Adjustments with Google Ads

Uploads conversion adjustments to Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId:uploadConversionAdjustments`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Upload Conversion Adjustments](https://developers.google.com/google-ads/api/reference/rpc/v22/ConversionAdjustmentUploadService/UploadConversionAdjustments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversionAdjustments[]` | body | `array` | yes | Conversion adjustment rows to upload. |
| `customerId` | path | `list` | yes | Customer ID that owns the Google Ads resources (without dashes). |
| `partialFailure` | body | `boolean` | yes | — |
| `validateOnly` | body | `boolean` | no | When true, validates the request without executing mutations. |
