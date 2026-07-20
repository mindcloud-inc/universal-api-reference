# Upload Call Conversions with Google Ads

Uploads call conversions to Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId:uploadCallConversions`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [Upload Call Conversions](https://developers.google.com/google-ads/api/reference/rpc/v22/ConversionUploadService/UploadCallConversions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversions[]` | body | `array` | yes | Call conversion rows to upload. |
| `customerId` | path | `list` | yes | Customer ID that owns the Google Ads resources (without dashes). |
| `partialFailure` | body | `boolean` | yes | — |
| `validateOnly` | body | `boolean` | no | When true, validates the request without executing mutations. |
