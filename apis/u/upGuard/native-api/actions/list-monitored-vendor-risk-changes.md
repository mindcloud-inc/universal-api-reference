# List Monitored Vendor Risk Changes with UpGuard

Retrieves risk changes for monitored vendors in UpGuard.

## Endpoint

- **Method:** `GET`
- **Path:** `/risks/vendors/diffs`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [List Monitored Vendor Risk Changes](https://cyber-risk.upguard.com/api/docs#operation/vendors_risks_diff)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | yes | The RFC 3339 start date used to calculate introduced and resolved risks. |
| `end_date` | query | `string` | no | The RFC 3339 end date used to calculate introduced and resolved risks. |
