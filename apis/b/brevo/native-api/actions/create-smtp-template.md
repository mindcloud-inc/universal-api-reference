# Create SMTP Template with Brevo

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/smtp/templates`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Create SMTP Template](https://developers.brevo.com/reference/create-smtp-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `htmlContent` | body | `string` | yes | HTML content for the template. |
| `replyTo` | body | `string` | yes | Reply-to email address. |
| `senderName` | body | `string` | yes | Display name of the template sender. |
| `subject` | body | `string` | yes | Default subject line for the template. |
| `templateName` | body | `string` | yes | Name of the SMTP template. |
| `toField` | body | `string` | no | Template to-field value. |
