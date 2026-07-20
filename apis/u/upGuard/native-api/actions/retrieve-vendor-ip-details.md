# Retrieve Vendor IP Details with UpGuard

Retrieves details for a vendor IP address in UpGuard.

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/ip`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [Retrieve Vendor IP Details](https://cyber-risk.upguard.com/api/docs#operation/vendor_ip_details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vendor_primary_hostname` | query | `string` | yes | The primary hostname of the vendor to show the IP detail for. |
| `ip` | query | `string` | yes | The IP address to retrieve details for. |
