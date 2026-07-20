# Verify Email Address with MailFloss

Verifies an email address with MailFloss.

## Endpoint

- **Method:** `GET`
- **Path:** `/verify`
- **Base URL:** `https://api.mailfloss.com`
- **Official documentation:** [Verify Email Address](https://developers.mailfloss.com/9bbG-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | The email address to verify. |
| `timeout` | query | `number` | no | Timeout in milliseconds. Max 60000; defaults to 30000. |
