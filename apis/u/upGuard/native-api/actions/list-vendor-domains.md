# List Vendor Domains with UpGuard

Retrieves domains for a monitored vendor in UpGuard.

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/domains`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [List Vendor Domains](https://cyber-risk.upguard.com/api/docs#operation/vendor_domains)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vendor_primary_hostname` | query | `string` | yes | The primary hostname of the vendor to list domains for. |
| `active` | query | `boolean` | no | Include active domains. |
| `inactive` | query | `boolean` | no | Include inactive domains. |
| `labels[]` | query | `array<string>` | no | Filter domains by the provided labels. Send multiple values as a string separated by `,`. |
