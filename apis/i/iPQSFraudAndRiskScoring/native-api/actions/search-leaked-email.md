# Search Leaked Email with IPQS Fraud and Risk Scoring

Retrieves dark web leak matches for an email from IPQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/leaked/email/{apiKey}/:email`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Search Leaked Email](https://www.ipqualityscore.com/documentation/dark-web-leak-api/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | Email address to search for in leaked data. |
