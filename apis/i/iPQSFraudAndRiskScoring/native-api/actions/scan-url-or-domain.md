# Scan URL Or Domain with IPQS Fraud and Risk Scoring

Retrieves malicious URL scan results from IPQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/url/{apiKey}/:url`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Scan URL Or Domain](https://www.ipqualityscore.com/documentation/malicious-url-scanner-api/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | path | `string` | yes | URL-encoded link or domain to scan. |
