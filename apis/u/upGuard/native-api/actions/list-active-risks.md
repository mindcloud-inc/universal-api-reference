# List Active Risks with UpGuard

Retrieves active risks for your UpGuard account.

## Endpoint

- **Method:** `GET`
- **Path:** `/risks`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [List Active Risks](https://cyber-risk.upguard.com/api/docs#operation/risks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `min_severity` | query | `string` | no | Minimum severity for the risks |
| `include_meta` | query | `boolean` | no | Include metadata for risks |
| `include_sources` | query | `boolean` | no | Include sources for risks, including hostname and IP data when available |
