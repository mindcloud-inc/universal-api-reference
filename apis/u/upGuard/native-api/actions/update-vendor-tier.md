# Update Vendor Tier with UpGuard

Updates the tier for a vendor in UpGuard.

## Endpoint

- **Method:** `PUT`
- **Path:** `/vendor/tier`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [Update Vendor Tier](https://cyber-risk.upguard.com/api/docs#operation/vendor_update_tier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vendor_primary_hostname` | query | `string` | yes | The primary hostname of the vendor to update tier for. |
| `tier` | query | `number` | yes | The tier to assign to the vendor. Use zero to remove the tier. |
