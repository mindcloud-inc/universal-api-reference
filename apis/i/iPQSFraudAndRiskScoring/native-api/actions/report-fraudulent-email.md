# Report Fraudulent Email with IPQS Fraud and Risk Scoring

Reports a fraudulent email address to IPQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/report/{apiKey}`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Report Fraudulent Email](https://www.ipqualityscore.com/documentation/fraud-reporting/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Email address to report. |
