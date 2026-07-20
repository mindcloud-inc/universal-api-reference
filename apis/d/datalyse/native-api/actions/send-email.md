# Send Email with Datalyse

Sends an email from Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/emails/send.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Send Email](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bcc` | body | `string` | no | BCC recipients (optional) |
| `cc` | body | `string` | no | CC recipients (optional) |
| `html` | body | `string` | yes | Email body in HTML |
| `lead_id` | body | `string` | no | Associate email with a contact ID (optional) |
| `opportunity_id` | body | `string` | no | Associate email with an opportunity ID (optional) |
| `signature_id` | body | `string` | no | Append this signature to the email (optional, get from signatures/get) |
| `subject` | body | `string` | yes | Email subject |
| `to` | body | `string` | yes | Recipient email address |
| `tracking` | body | `string` | no | Enable open tracking, set to "y" (optional) |
