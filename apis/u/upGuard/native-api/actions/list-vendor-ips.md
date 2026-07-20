# List Vendor IPs with UpGuard

Retrieves IP addresses for a vendor in UpGuard.

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/ips`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [List Vendor IPs](https://cyber-risk.upguard.com/api/docs#operation/vendor_ips)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vendor_primary_hostname` | query | `string` | yes | The primary hostname of the vendor to list IPs for. |
