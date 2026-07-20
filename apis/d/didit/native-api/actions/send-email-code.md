# Send Email Code with Didit

Sends an email verification code in Didit.

## Endpoint

- **Method:** `POST`
- **Path:** `https://verification.didit.me/v3/email/send/`
- **Base URL:** `https://verification.didit.me/v3`
- **Official documentation:** [Send Email Code](https://docs.didit.me/standalone-apis/email-send)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to verify. |
