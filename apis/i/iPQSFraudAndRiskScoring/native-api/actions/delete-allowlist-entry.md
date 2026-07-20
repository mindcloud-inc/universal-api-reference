# Delete Allowlist Entry with IPQS Fraud and Risk Scoring

Deletes an existing allowlist entry from IPQS.

## Endpoint

- **Method:** `POST`
- **Path:** `/allowlist/delete/{apiKey}`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Delete Allowlist Entry](https://www.ipqualityscore.com/documentation/allowlist-api/allowlist-deleting-entries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | body | `string` | yes | Value to remove from the allowlist. |
