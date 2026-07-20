# Delete Blocklist Entry with IPQS Fraud and Risk Scoring

Deletes an existing blocklist entry from IPQS.

## Endpoint

- **Method:** `POST`
- **Path:** `/blocklist/delete/{apiKey}`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Delete Blocklist Entry](https://www.ipqualityscore.com/documentation/allowlist-api/blocklist-deleting-entries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | body | `string` | yes | Value to remove from the blocklist. |
