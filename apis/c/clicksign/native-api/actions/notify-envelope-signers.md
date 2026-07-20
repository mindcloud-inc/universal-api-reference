# Notify Envelope Signers with Clicksign

Notifies signers for a Clicksign envelope.

## Endpoint

- **Method:** `POST`
- **Path:** `/envelopes/:envelope_id/notifications`
- **Base URL:** `https://app.clicksign.com/api/v3`
- **Official documentation:** [Notify Envelope Signers](https://developers.clicksign.com/reference/api-notificar-envelope)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | no | JSON:API document wrapper. |
| `envelope_id` | path | `string` | yes | The UUID of the envelope. |
| `data.attributes` | body | `object` | no | Notification attributes. |
| `data.attributes.message` | body | `string` | no | Message sent to the signer. If omitted, Clicksign uses the envelope default message. |
| `email_customization` | body | `object` | no | Custom email notification settings. |
| `data.attributes.emailCustomization.subject` | body | `string` | no | Custom email subject. |
| `data.attributes.emailCustomization.head` | body | `string` | no | Custom email header text. |
| `data.attributes.emailCustomization.greeting` | body | `string` | no | Custom email greeting. |
| `data.attributes.emailCustomization.principal` | body | `string` | no | Custom main email message. |
| `data.attributes.emailCustomization.button` | body | `string` | no | Custom button label in the email. |
| `data.attributes.emailCustomization.final` | body | `string` | no | Custom final email message after the button. |
| `data.attributes.emailCustomization.align` | body | `string` | no | Email content alignment. |
| `show_token` | body | `boolean` | no | Whether to show the token in the email body when token authentication exists. |
| `show_qrcode` | body | `boolean` | no | Whether to include a QR code pointing to the signing link. |
| `show_details` | body | `boolean` | no | Whether to show signature-process details in the email. |
