# Validate Email with IPQS Fraud and Risk Scoring

Retrieves email validation and fraud data from IPQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/email/{apiKey}/:email`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Validate Email](https://www.ipqualityscore.com/documentation/email-validation-api/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | Email address to validate. |
