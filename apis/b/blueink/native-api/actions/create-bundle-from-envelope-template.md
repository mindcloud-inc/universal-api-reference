# Create Bundle from Envelope Template with Blueink

Creates a Blueink bundle from an envelope template.

## Endpoint

- **Method:** `POST`
- **Path:** `/bundles/create_from_envelope_template/`
- **Base URL:** `https://api.blueink.com/api/v2`
- **Official documentation:** [Create Bundle from Envelope Template](https://developer.blueink.com/api/#tag/Bundles/operation/createBundleFromEnvelopeTemplate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `label` | body | `string` | no | A label to help you identify this Bundle |
| `is_test` | body | `boolean` | no | Set to true while the integration is under development |
| `status` | body | `string` | no | Leave blank to send normally or use dr to create a draft bundle |
| `envelope_template.template_id` | body | `string` | yes | The envelope template identifier to instantiate |
| `packets[].key` | body | `string` | yes | The signer role key from the envelope template |
| `packets[].name` | body | `string` | yes | The recipient name for this packet |
| `packets[].email` | body | `string` | yes | The recipient email address for this packet |
| `packets[].phone` | body | `string` | no | The recipient phone number for this packet when SMS delivery or SMS auth is used |
| `packets[].deliver_via` | body | `string` | no | How Blueink should deliver the signing request |
