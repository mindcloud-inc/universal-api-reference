# Create Blocklist Entry with IPQS Fraud and Risk Scoring

Creates a new blocklist entry in IPQS.

## Endpoint

- **Method:** `POST`
- **Path:** `/blocklist/create/{apiKey}`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Create Blocklist Entry](https://www.ipqualityscore.com/documentation/allowlist-api/blocklist-creating-entries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | body | `string` | yes | Value to add to the blocklist. |
| `reason` | body | `string` | no | Reason for adding the blocklist entry. |
