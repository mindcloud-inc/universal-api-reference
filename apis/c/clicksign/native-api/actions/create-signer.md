# Create Signer with Clicksign

Creates a signer in a Clicksign envelope.

## Endpoint

- **Method:** `POST`
- **Path:** `/envelopes/:envelope_id/signers`
- **Base URL:** `https://app.clicksign.com/api/v3`
- **Official documentation:** [Create Signer](https://developers.clicksign.com/reference/api-criar-signatario)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | no | JSON:API document wrapper. |
| `data.attributes` | body | `object` | no | Signer attributes. |
| `data.attributes.birthday` | body | `date` | no | The signer birth date. |
| `data.attributes.communicateEvents` | body | `object` | no | Notification channel settings. |
| `data.attributes.documentation` | body | `string` | no | The signer documentation number. |
| `data.attributes.email` | body | `string` | yes | The signer email address. |
| `data.attributes.group` | body | `number` | no | The signer group number. |
| `data.attributes.name` | body | `string` | yes | The signer name. |
| `data.attributes.refusable` | body | `boolean` | no | Whether the signer can refuse. |
| `document_signed` | body | `string` | no | Delivery channel for signed-document notices. |
| `envelope_id` | path | `string` | yes | The UUID of the envelope. |
| `has_documentation` | body | `boolean` | no | Whether signer documentation is provided. |
| `location_required_enabled` | body | `boolean` | no | Whether signer geolocation is required. |
| `phone_number` | body | `string` | no | The signer phone number. |
| `signature_reminder` | body | `string` | no | Delivery channel for signature reminders. |
| `signature_request` | body | `string` | no | Delivery channel for signature requests. |
