# Upload Sale with Dripcel

Creates a sale in Dripcel.

## Endpoint

- **Method:** `GET`
- **Path:** `/sales/create`
- **Base URL:** `https://api.dripcel.com`
- **Official documentation:** [Upload Sale](https://docs.dripcel.com/API/sales#get-request)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `campaign_id` | query | `string` | yes |
| `cell` | query | `string` | yes |
| `click_id` | query | `string` | no |
| `saleValue` | query | `string` | no |
| `send_id` | query | `string` | no |
| `soldAt` | query | `string` | no |
