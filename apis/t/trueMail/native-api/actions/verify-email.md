# Verify Email with TrueMail

Validates an email address in TrueMail.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/verify`
- **Base URL:** `https://api.mailcop.net`
- **Official documentation:** [Verify Email](https://mailcop.net/docs/api-verify)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address to validate. |
| `validation_type` | body | `string` | no | Choose MX for standard validation or SMTP for premium mailbox checks. Accepted values: `0`, `1`. |
