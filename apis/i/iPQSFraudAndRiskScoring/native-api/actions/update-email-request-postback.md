# Update Email Request Postback with IPQS Fraud and Risk Scoring

Updates email validation request postback data in IPQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/postback/{apiKey}`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Update Email Request Postback](https://www.ipqualityscore.com/documentation/email-validation-api/conversions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | query | `string` | yes | Original email request ID to update. |
| `update[ConversionStatus]` | query | `boolean` | no | Conversion status update value. |
