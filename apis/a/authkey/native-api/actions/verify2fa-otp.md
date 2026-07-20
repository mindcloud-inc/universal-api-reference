# Verify 2FA OTP with Authkey

Verifies a 2FA OTP in Authkey.

## Endpoint

- **Method:** `GET`
- **Path:** `https://console.authkey.io/api/2fa_verify.php`
- **Base URL:** `https://console.authkey.io/restapi`
- **Official documentation:** [Verify 2FA OTP](https://authkey.io/2fa-api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | query | `string` | yes | Verification channel: SMS, VOICE, or EMAIL. |
| `otp` | query | `string` | yes | OTP code entered by the customer. |
| `logid` | query | `string` | yes | Log ID returned by the Start 2FA Session action. |
