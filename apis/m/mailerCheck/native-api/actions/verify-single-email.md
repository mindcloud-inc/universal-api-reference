# Verify Single Email with MailerCheck

Retrieves a real-time email verification result from MailerCheck.

## Endpoint

- **Method:** `POST`
- **Path:** `/check/single`
- **Base URL:** `https://app.mailercheck.com/api`
- **Official documentation:** [Verify Single Email](https://developers.mailercheck.com/email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to verify. |
