# Create Verification List with MailerCheck

Creates a verification list in MailerCheck.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists`
- **Base URL:** `https://app.mailercheck.com/api`
- **Official documentation:** [Create Verification List](https://developers.mailercheck.com/email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Verification list name. |
| `emails[]` | body | `array<string>` | yes | Email addresses to add to the verification list. |
