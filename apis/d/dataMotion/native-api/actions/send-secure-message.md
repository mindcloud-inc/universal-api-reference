# Send Secure Message with DataMotion

Sends a secure message through DataMotion.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.2/Email`
- **Base URL:** `https://api.datamotion.com/SecureMessageDelivery`
- **Official documentation:** [Send Secure Message](https://datamotion.com/guide-to-secure-message-delivery-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `From` | body | `string` | yes | Email address of the DataMotion user sending the secure message. |
| `To[]` | body | `array<string>` | no | Recipients of the secure message. Send multiple values as a array. |
| `Cc[]` | body | `array<string>` | no | Recipients copied on the secure message. Send multiple values as a array. |
| `Bcc[]` | body | `array<string>` | no | Recipients blind-copied on the secure message. Send multiple values as a array. |
| `Subject` | body | `string` | no | Subject of the secure message. |
| `TextBody` | body | `string` | no | Plain text body of the secure message. |
| `HtmlBody` | body | `string` | no | HTML body of the secure message. |
| `Attachments[]` | body | `array<object>` | no | Array of attachment objects with AttachmentBase64, ContentType, FileName, and optional ContentId. |
