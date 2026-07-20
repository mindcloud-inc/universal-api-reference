# List Monitored Vendors with UpGuard

Retrieves monitored vendors from your UpGuard portfolio.

## Endpoint

- **Method:** `GET`
- **Path:** `/vendors`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [List Monitored Vendors](https://cyber-risk.upguard.com/api/docs#operation/vendors)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_ad_hoc_reports` | query | `boolean` | no | Include vendors that already have an ad hoc report in the results. |
| `labels[]` | query | `array<string>` | no | Filter vendors by the provided labels. Send multiple values as a string separated by `,`. |
| `include_risks` | query | `boolean` | no | Include risks in each vendor result. |
