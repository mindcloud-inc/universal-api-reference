# Validate Phone Number with IPQS Fraud and Risk Scoring

Retrieves phone validation and carrier details from IPQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/phone/{apiKey}/:phone`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Validate Phone Number](https://www.ipqualityscore.com/documentation/phone-number-validation-api/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | path | `string` | yes | Phone number to validate. |
| `country` | query | `string` | no | Country code context for phone validation. |
