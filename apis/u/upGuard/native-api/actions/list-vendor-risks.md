# List Vendor Risks with UpGuard

Retrieves active risks for a vendor in UpGuard.

## Endpoint

- **Method:** `GET`
- **Path:** `/risks/vendors`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [List Vendor Risks](https://cyber-risk.upguard.com/api/docs#operation/vendor_risks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `primary_hostname` | query | `string` | yes | The primary hostname of the vendor to return risks for. |
