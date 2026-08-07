# Upload Click Conversions with Google Ads

Uploads click conversions to Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId:uploadClickConversions`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Upload Click Conversions](https://developers.google.com/google-ads/api/reference/rpc/v22/ConversionUploadService/UploadClickConversions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversions[]` | body | `array` | yes | Click conversion rows to upload. |
| `customerId` | path | `list` | yes | Customer ID that owns the Google Ads resources (without dashes). |
| `partialFailure` | body | `boolean` | yes | — |
| `validateOnly` | body | `boolean` | no | When true, validates the request without executing mutations. |
