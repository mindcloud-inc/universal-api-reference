# Search Leaked Password with IPQS Fraud and Risk Scoring

Retrieves dark web leak matches for a password from IPQS.

## Endpoint

- **Method:** `POST`
- **Path:** `/leaked/password/{apiKey}`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Search Leaked Password](https://www.ipqualityscore.com/documentation/dark-web-leak-api/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `password` | body | `string` | yes | Plain-text or hashed password to submit in the POST body per IPQS docs. |
