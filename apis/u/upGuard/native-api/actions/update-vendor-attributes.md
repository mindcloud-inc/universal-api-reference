# Update Vendor Attributes with UpGuard

Updates attributes for a vendor in UpGuard.

## Endpoint

- **Method:** `PUT`
- **Path:** `/vendor/attributes`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [Update Vendor Attributes](https://cyber-risk.upguard.com/api/docs#operation/vendor_update_attributes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vendor_primary_hostname` | body | `string` | yes | The primary hostname of the vendor to update attributes for. |
| `attributes` | body | `object` | no | Attributes to assign to the vendor. Use null to reset an attribute value. |
