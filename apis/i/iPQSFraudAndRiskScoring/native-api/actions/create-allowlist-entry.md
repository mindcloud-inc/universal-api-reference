# Create Allowlist Entry with IPQS Fraud and Risk Scoring

Creates a new allowlist entry in IPQS.

## Endpoint

- **Method:** `POST`
- **Path:** `/allowlist/create/{apiKey}`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Create Allowlist Entry](https://www.ipqualityscore.com/documentation/allowlist-api/allowlist-creating-entries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | body | `string` | yes | Value to add to the allowlist. |
| `reason` | body | `string` | no | Reason for adding the allowlist entry. |
