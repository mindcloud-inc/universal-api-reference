# Send Signature Request with Template with Dropbox Sign

Creates a signature request from a template in Dropbox Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/signature_request/send_with_template`
- **Base URL:** `https://api.hellosign.com/v3`
- **Official documentation:** [Send Signature Request with Template](https://developers.hellosign.com/api/reference/operation/signatureRequestSendWithTemplate/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | no | The email message sent to signers. |
| `signers[].email_address` | body | `string` | yes | The email address of the signer. |
| `signers[].name` | body | `string` | yes | The name of the signer. |
| `signers[].role` | body | `string` | yes | Must match an existing signer role in the selected template. |
| `subject` | body | `string` | no | The email subject sent to signers. |
| `template_ids[]` | body | `array<string>` | yes | One or more template IDs used to create the signature request. |
| `test_mode` | body | `boolean` | no | Whether to create the signature request in test mode. |
| `title` | body | `string` | no | The title to assign to the signature request. |
