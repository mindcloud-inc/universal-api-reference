# Search Leaked Email And Password with IPQS Fraud and Risk Scoring

Retrieves dark web leak matches for an email-password pair from IPQS.

## Endpoint

- **Method:** `POST`
- **Path:** `/leaked/emailpass/{apiKey}`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Search Leaked Email And Password](https://www.ipqualityscore.com/documentation/dark-web-leak-api/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to pair with the password for leaked credential search. |
| `password` | body | `string` | yes | Plain-text or hashed password to submit in the POST body per IPQS docs. |
