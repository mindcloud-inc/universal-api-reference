# Verify Raw Email Authenticity with Mailcheck

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/verify/auth`
- **Base URL:** `https://api.mailcheck.dev`
- **Official documentation:** [Verify Raw Email Authenticity](https://api.mailcheck.dev/docs#verify-auth)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `raw_email` | body | `string` | yes | Full raw email source. MailCheck strips the body and analyzes only the headers. |
| `trusted_domains[]` | body | `array<string>` | no | Optional list of trusted domains used for lookalike detection. Provide a JSON array of domain strings. |
