# Retrieve Vendor Domain Details with UpGuard

Retrieves details for a vendor domain in UpGuard.

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/domain`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [Retrieve Vendor Domain Details](https://cyber-risk.upguard.com/api/docs#operation/vendor_domain_details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vendor_primary_hostname` | query | `string` | yes | The primary hostname of the vendor to show the domain detail for. |
| `hostname` | query | `string` | yes | The domain hostname for which to return details. |
