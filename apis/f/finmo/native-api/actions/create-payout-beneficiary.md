# Create Payout Beneficiary with Finmo

Creates a new payout beneficiary in Finmo.

## Endpoint

- **Method:** `POST`
- **Path:** `/payout-beneficiary`
- **Base URL:** `https://api.finmo.net/v1/`
- **Official documentation:** [Create Payout Beneficiary](https://docs.finmo.net/reference/newpayoutbeneficiarycompany-1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `type` | body | `string` | yes |
| `beneficiary_name` | body | `string` | yes |
| `currency` | body | `string` | no |
| `company` | body | `object` | no |
| `individual` | body | `object` | no |
| `description` | body | `string` | no |
| `bank_country` | body | `string` | no |
| `bank_name` | body | `string` | no |
| `account_number` | body | `string` | no |
| `bsb` | body | `string` | no |
| `bic_swift` | body | `string` | no |
| `intermediary_bic_swift` | body | `string` | no |
| `iban` | body | `string` | no |
| `aba` | body | `string` | no |
| `sort_code` | body | `string` | no |
| `pay_id` | body | `string` | no |
| `pay_id_type` | body | `string` | no |
| `ifsc` | body | `string` | no |
| `branch_code` | body | `string` | no |
| `bank_code` | body | `string` | no |
| `organization_reference_id` | body | `string` | no |
| `metadata` | body | `object` | no |
| `proxy_type` | body | `string` | no |
| `proxy_value` | body | `string` | no |
| `payout_beneficiary_controls` | body | `object` | no |
