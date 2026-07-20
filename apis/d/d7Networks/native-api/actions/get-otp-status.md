# Get OTP Status with D7 Networks

Retrieves OTP verification status from D7 Networks.

## Endpoint

- **Method:** `GET`
- **Path:** `/verify/v1/report/:otpId`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Get OTP Status](https://d7networks.com/docs/verify/get-status/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `otp_id` | path | `string` | yes | OTP ID returned by the Send OTP or Resend OTP action. |
