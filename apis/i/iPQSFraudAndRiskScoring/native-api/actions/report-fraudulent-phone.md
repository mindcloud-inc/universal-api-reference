# Report Fraudulent Phone with IPQS Fraud and Risk Scoring

Reports a fraudulent phone number to IPQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/report/{apiKey}`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Report Fraudulent Phone](https://www.ipqualityscore.com/documentation/fraud-reporting/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | query | `string` | yes | Phone number to report. |
| `country` | query | `string` | yes | Two-letter country code or full country name for the phone report. |
