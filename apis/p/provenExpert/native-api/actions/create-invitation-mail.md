# Create Invitation Mail with ProvenExpert

Creates and sends survey invitation emails in ProvenExpert.

## Endpoint

- **Method:** `POST`
- **Path:** `/invite/mail/create`
- **Base URL:** `https://www.provenexpert.com/api/v1`
- **Official documentation:** [Create Invitation Mail](https://developer.provenexpert.com/index_en.html#invite-mail-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.code` | body | `string` | yes | Survey code for which invitation emails should be created. |
| `data.reminder` | body | `number` | no | Whether ProvenExpert should send a reminder email after 7 days. Provider default is 1 when omitted. |
| `data.recipients[]` | body | `array<object>` | yes | Recipient list for the invitation mailing. |
| `data.recipients[].email` | body | `string` | yes | Email address of the recipient. |
| `data.recipients[].name` | body | `string` | no | Name of the recipient. |
| `data.recipients[].subject` | body | `string` | no | Custom email subject for the invitation email. |
| `data.recipients[].salutation` | body | `string` | no | Custom salutation in the invitation email. |
| `data.recipients[].text` | body | `string` | no | Custom invitation email body text. |
| `data.recipients[].reminderSubject` | body | `string` | no | Custom subject for the reminder email. |
| `data.recipients[].reminderSalutation` | body | `string` | no | Custom salutation in the reminder email. |
| `data.recipients[].reminderText` | body | `string` | no | Custom reminder email body text. |
