# List Vendor Vulnerabilities with UpGuard

Retrieves potential vulnerabilities for a vendor in UpGuard.

## Endpoint

- **Method:** `GET`
- **Path:** `/vulnerabilities/vendor`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [List Vendor Vulnerabilities](https://cyber-risk.upguard.com/api/docs#operation/vendor_vulnerabilities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `primary_hostname` | query | `string` | yes | The primary hostname of the vendor to return vulnerabilities for. |
