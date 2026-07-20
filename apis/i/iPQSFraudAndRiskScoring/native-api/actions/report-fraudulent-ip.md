# Report Fraudulent IP with IPQS Fraud and Risk Scoring

Reports a fraudulent IP address to IPQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/report/{apiKey}`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Report Fraudulent IP](https://www.ipqualityscore.com/documentation/fraud-reporting/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | query | `string` | yes | IPv4 or IPv6 address to report. |
