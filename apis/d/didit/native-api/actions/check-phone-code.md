# Check Phone Code with Didit

Checks a phone verification code in Didit.

## Endpoint

- **Method:** `POST`
- **Path:** `https://verification.didit.me/v3/phone/check/`
- **Base URL:** `https://verification.didit.me/v3`
- **Official documentation:** [Check Phone Code](https://docs.didit.me/standalone-apis/phone-check)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | Verification code received by phone. |
| `phone_number` | body | `string` | yes | Phone number used during verification. |
