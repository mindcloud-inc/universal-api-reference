# Create Account with Instantly

Creates a new account in Instantly.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/accounts`
- **Base URL:** `https://api.instantly.ai`
- **Official documentation:** [Create Account](https://developer.instantly.ai/api/v2/account/createaccount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address of the account. |
| `first_name` | body | `string` | yes | First name associated with the account. |
| `last_name` | body | `string` | yes | Last name associated with the account. |
| `provider_code` | body | `number` | yes | Provider code for the account: 1 Custom IMAP/SMTP, 2 Google, 3 Microsoft, 4 AWS, 8 AirMail. |
| `imap_username` | body | `string` | yes | IMAP username. |
| `imap_password` | body | `string` | yes | IMAP password. |
| `imap_host` | body | `string` | yes | IMAP host. |
| `imap_port` | body | `number` | yes | IMAP port. |
| `smtp_username` | body | `string` | yes | SMTP username. |
| `smtp_password` | body | `string` | yes | SMTP password. |
| `smtp_host` | body | `string` | yes | SMTP host. |
| `smtp_port` | body | `number` | yes | SMTP port. |
