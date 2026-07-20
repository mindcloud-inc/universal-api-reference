# Verify Email MX with TrueMail

Validates an email address with MX checks in TrueMail.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/verify`
- **Base URL:** `https://api.mailcop.net`
- **Official documentation:** [Verify Email MX](https://mailcop.net/docs/api-verify)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address to validate. |
