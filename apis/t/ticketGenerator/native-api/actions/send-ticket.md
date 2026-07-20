# Send Ticket with Ticket Generator

Sends a ticket by email, SMS, or WhatsApp in Ticket Generator.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/ticket/send/`
- **Base URL:** `https://apis.ticket-generator.com/client`
- **Official documentation:** [Send Ticket](https://apis.ticket-generator.com/client/api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | query | `string` | yes | Ticket Generator event identifier. |
| `ticketCategoryId` | query | `string` | no | Ticket category identifier. Optional when the event has exactly one ticket category. |
| `email` | body | `string` | no | Recipient email address. |
| `phoneNumber` | body | `string` | no | Recipient phone number in E.164 format. |
| `whatsApp` | body | `boolean` | no | Send the ticket over WhatsApp instead of SMS when a phone number is provided. |
| `whatsAppConsent` | body | `boolean` | no | Confirms the recipient consented to receive the ticket on WhatsApp. |
| `subject` | body | `string` | no | Email subject line. Maximum length: 100. |
| `body` | body | `string` | no | Email body content. |
| `fromName` | body | `string` | no | Sender name displayed in the email. Maximum length: 50. |
| `header_1` | body | `string` | no | Variable information field label 1. |
| `value_1` | body | `string` | no | Variable information field value 1. |
| `header_2` | body | `string` | no | Variable information field label 2. |
| `value_2` | body | `string` | no | Variable information field value 2. |
| `header_3` | body | `string` | no | Variable information field label 3. |
| `value_3` | body | `string` | no | Variable information field value 3. |
| `header_4` | body | `string` | no | Variable information field label 4. |
| `value_4` | body | `string` | no | Variable information field value 4. |
| `header_5` | body | `string` | no | Variable information field label 5. |
| `value_5` | body | `string` | no | Variable information field value 5. |
