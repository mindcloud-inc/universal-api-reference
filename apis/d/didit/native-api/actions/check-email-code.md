# Check Email Code with Didit

Checks an email verification code in Didit.

## Endpoint

- **Method:** `POST`
- **Path:** `https://verification.didit.me/v3/email/check/`
- **Base URL:** `https://verification.didit.me/v3`
- **Official documentation:** [Check Email Code](https://docs.didit.me/standalone-apis/email-check)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | Verification code received by email. |
| `email` | body | `string` | yes | Email address used during verification. |
