# List Business Accounts with Chargback

## Endpoint

- **Method:** `GET`
- **Path:** `/api/public/v1/business_accounts/`
- **Base URL:** `https://api.chargeback.io`
- **Official documentation:** [List Business Accounts](https://api.chargeback.io/api/public/docs/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page` | query | `number` | no |
| `page_size` | query | `number` | no |
| `ordered_by` | query | `string` | no |
| `name` | query | `string` | no |
| `is_active` | query | `boolean` | no |
| `base_currency` | query | `string` | no |
