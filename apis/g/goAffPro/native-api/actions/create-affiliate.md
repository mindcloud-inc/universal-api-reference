# Create Affiliate with GoAffPro

Creates a new affiliate in GoAffPro.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/affiliates`
- **Base URL:** `https://api.goaffpro.com/v1`
- **Official documentation:** [Create Affiliate](https://api.goaffpro.com/docs/admin/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Affiliate email address. |
| `name` | body | `string` | no | Affiliate display name. |
| `ref_code` | body | `string` | no | Referral code for the affiliate. |
| `status` | body | `string` | no | Affiliate approval status. |
