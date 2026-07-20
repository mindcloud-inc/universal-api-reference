# Send a transactional email with raw data with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/emails/transaction`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Send a transactional email with raw data](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_address` | body | `string` | no | — |
| `subject` | body | `string` | no | — |
| `html` | body | `string` | no | — |
| `bcc[]` | body | `array<string>` | no | List of BCC email addresses Send multiple values as a array. |
| `variables` | body | `object` | no | Template for mailgun variables for substitution or Mumara for personalization |
| `provider` | body | `string` | no | Email service provider to use |
