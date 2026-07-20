# Update Affiliate with GoAffPro

Updates an existing affiliate in GoAffPro.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/admin/affiliates/:id`
- **Base URL:** `https://api.goaffpro.com/v1`
- **Official documentation:** [Update Affiliate](https://api.goaffpro.com/docs/admin/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Affiliate ID. |
| `name` | body | `string` | no | Affiliate display name. |
| `ref_code` | body | `string` | no | Referral code for the affiliate. |
| `status` | body | `string` | no | Affiliate approval status. |
