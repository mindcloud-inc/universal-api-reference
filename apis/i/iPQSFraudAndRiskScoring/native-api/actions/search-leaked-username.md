# Search Leaked Username with IPQS Fraud and Risk Scoring

Retrieves dark web leak matches for a username from IPQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/leaked/username/{apiKey}/:username`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Search Leaked Username](https://www.ipqualityscore.com/documentation/dark-web-leak-api/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Username to search for in leaked data. |
