# Update Proxy Request Postback with IPQS Fraud and Risk Scoring

Updates proxy detection request postback data in IPQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/postback/{apiKey}`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Update Proxy Request Postback](https://www.ipqualityscore.com/documentation/proxy-detection-api/conversions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | query | `string` | yes | Original proxy request ID to update. |
| `update[ConversionStatus]` | query | `boolean` | no | Conversion status update value. |
