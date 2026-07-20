# Report Fraudulent Request with IPQS Fraud and Risk Scoring

Reports a fraudulent event to IPQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/report/{apiKey}`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Report Fraudulent Request](https://www.ipqualityscore.com/documentation/fraud-reporting/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | query | `string` | yes | Previous IPQS request ID to report. |
