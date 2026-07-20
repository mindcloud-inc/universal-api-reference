# Send Email Message with LaGrowthMachine

Sends an email message to a lead in LaGrowthMachine.

## Endpoint

- **Method:** `POST`
- **Path:** `/inbox/email`
- **Base URL:** `https://apiv2.lagrowthmachine.com/flow`
- **Official documentation:** [Send Email Message](https://documenter.getpostman.com/view/2071164/TVCmSkH2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bcc` | body | `string` | no | Comma-separated BCC recipients. |
| `cc` | body | `string` | no | Comma-separated CC recipients. |
| `identityId` | body | `string` | yes | Email identity that sends the message. |
| `leadEmail` | body | `string` | no | Target lead email. Provide either Lead ID or Lead Email. |
| `leadId` | body | `string` | no | Target lead ID. Provide either Lead ID or Lead Email. |
| `message.html` | body | `string` | yes | HTML version of the email body. |
| `message.text` | body | `string` | yes | Plain-text version of the email body. |
| `replyInLastThread` | body | `boolean` | no | Whether to reply in the latest thread. |
| `replyToMessageId` | body | `string` | no | Specific message ID to reply to. |
| `subject` | body | `string` | no | Email subject when not replying in thread. |
