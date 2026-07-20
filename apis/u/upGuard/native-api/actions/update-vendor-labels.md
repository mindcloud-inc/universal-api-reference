# Update Vendor Labels with UpGuard

Updates labels for a vendor in UpGuard.

## Endpoint

- **Method:** `PUT`
- **Path:** `/vendor/labels`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [Update Vendor Labels](https://cyber-risk.upguard.com/api/docs#operation/vendor_update_labels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vendor_primary_hostname` | query | `string` | yes | The primary hostname of the vendor to update labels for. |
| `labels` | query | `string<string>` | yes | The labels to assign to the vendor. Pass an empty array to remove all labels. |
