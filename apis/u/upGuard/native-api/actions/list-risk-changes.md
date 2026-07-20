# List Risk Changes with UpGuard

Retrieves risk changes for your UpGuard account.

## Endpoint

- **Method:** `GET`
- **Path:** `/risks/diff`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [List Risk Changes](https://cyber-risk.upguard.com/api/docs#operation/org_risks_diff)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `date` | yes | The starting point for determining risks introduced or resolved (RFC 3339 format) |
| `end_date` | query | `date` | no | The final state for determining risks introduced or resolved (RFC 3339 format) |
| `include_sources` | query | `boolean` | no | Include sources for risks, including hostname and IP data when available |
