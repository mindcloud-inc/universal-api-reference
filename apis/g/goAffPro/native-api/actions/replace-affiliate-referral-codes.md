# Replace Affiliate Referral Codes with GoAffPro

Replaces an affiliate's referral codes in GoAffPro.

## Endpoint

- **Method:** `PUT`
- **Path:** `/admin/affiliates/:id/referral_codes`
- **Base URL:** `https://api.goaffpro.com/v1`
- **Official documentation:** [Replace Affiliate Referral Codes](https://api.goaffpro.com/docs/admin/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Affiliate ID for the referral codes being replaced. |
| `referral_codes[]` | body | `array<string>` | yes | Referral codes to assign to the affiliate. |
