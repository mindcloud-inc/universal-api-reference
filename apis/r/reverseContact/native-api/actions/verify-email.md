# Verify Email with Reverse Contact

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/contact/email/verify`
- **Base URL:** `https://api.reversecontact.com`
- **Official documentation:** [Verify Email](https://app.reversecontact.com/docs/endpoints/contact-email-verify)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to verify. |
| `webhookUrl` | body | `string` | no | HTTPS callback URL for async results. |
