# List Crunchbase Funding Rounds with Piloterr

## Endpoint

- **Method:** `GET`
- **Path:** `/crunchbase/funding_rounds`
- **Base URL:** `https://api.piloterr.com/v2`
- **Official documentation:** [List Crunchbase Funding Rounds](https://docs.piloterr.com/crunchbase-funding-rounds)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `days_since_announcement` | query | `string` | no | Limit rounds announced within the last N days. |
| `funded_organization_identifier` | query | `string` | no | Crunchbase organization UUID to filter rounds. |
| `investment_type` | query | `string` | no | Crunchbase funding round type filter. |
