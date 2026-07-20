# Verify Email Authenticity with Mailcheck

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/verify/auth`
- **Base URL:** `https://api.mailcheck.dev`
- **Official documentation:** [Verify Email Authenticity](https://api.mailcheck.dev/docs#verify-auth)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `headers` | body | `string` | yes | Raw email header block to analyze for authenticity. |
| `trusted_domains[]` | body | `array<string>` | no | Optional list of trusted domains used for lookalike detection. Provide a JSON array of domain strings. |
