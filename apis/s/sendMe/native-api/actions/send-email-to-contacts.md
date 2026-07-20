# Send Email to Contacts with SendMe

## Endpoint

- **Method:** `POST`
- **Path:** `/api/messages/email/contacts`
- **Base URL:** `https://app.sendme123.com`
- **Official documentation:** [Send Email to Contacts](https://docs.sendme123.com/en/api/messages/email-contacts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts[]` | body | `array<string>` | yes | List of email addresses. Send multiple values as a array. |
| `message` | body | `string` | yes | Email content. |
| `subject` | body | `string` | yes | Email subject. |
