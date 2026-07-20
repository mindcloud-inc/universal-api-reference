# Create Email Template with Infobip

## Endpoint

- **Method:** `POST`
- **Path:** `/email/1/templates`
- **Base URL:** `https://rkpzwe.api.infobip.com`
- **Official documentation:** [Create Email Template](https://www.infobip.com/docs/api/channels/email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Name of the email template. |
| `from` | body | `string` | no | Email address with optional sender name. |
| `replyTo` | body | `string` | no | Email address to which recipients of the email can reply. |
| `subject` | body | `string` | no | Subject of the email template. |
| `preheader` | body | `string` | no | Preheader of the email template. |
| `html` | body | `string` | yes | HTML content of the email template. |
| `attachments` | body | `string` | no | JSON string of attachments to be sent with the email template. |
| `landingPage` | body | `string` | no | The identifier of an opt out landing late to be used and displayed when an end user clicks the unsubscribe link. Create a landing page in your Infobip account and use the ID number. For example, 1_23456. If not present, the default opt out landing page is used. |
