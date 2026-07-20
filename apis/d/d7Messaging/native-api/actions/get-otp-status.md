# Get OTP Status with D7 Messaging

Retrieves OTP status from D7 Messaging.

## Endpoint

- **Method:** `GET`
- **Path:** `/verify/v1/report/:otp_id`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Get OTP Status](https://d7networks.com/docs/verify/get-status/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `otp_id` | path | `string` | yes | OTP ID returned by Send OTP. |
