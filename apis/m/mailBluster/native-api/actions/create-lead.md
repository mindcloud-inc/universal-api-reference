# Create Lead with MailBluster

Creates a new lead in MailBluster.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads`
- **Base URL:** `https://api.mailbluster.com/api`
- **Official documentation:** [Create Lead](https://app.mailbluster.com/api-doc/leads/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address of the lead. |
| `subscribed` | body | `boolean` | yes | Whether the lead is subscribed to receive email. |
| `firstName` | body | `string` | no | First name of the lead. |
| `lastName` | body | `string` | no | Last name of the lead. |
| `doubleOptIn` | body | `boolean` | no | If true, MailBluster sends an opt-in confirmation email; keep false for direct create flows unless intentionally needed. |
