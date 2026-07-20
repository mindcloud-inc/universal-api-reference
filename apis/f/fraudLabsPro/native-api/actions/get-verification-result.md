# Get Verification Result with FraudLabs Pro

Retrieves an SMS verification result from FraudLabs Pro.

## Endpoint

- **Method:** `GET`
- **Path:** `v2/verification/result`
- **Base URL:** `https://api.fraudlabspro.com/`
- **Official documentation:** [Get Verification Result](https://www.fraudlabspro.com/developer/api/get-sms-verification-result)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tran_id` | query | `string` | yes | The transaction id returned by Send SMS Verification. |
| `otp` | query | `string` | yes | The one-time password received by the user. |
