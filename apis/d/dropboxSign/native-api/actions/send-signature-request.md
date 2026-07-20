# Send Signature Request with Dropbox Sign

Creates a signature request in Dropbox Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/signature_request/send`
- **Base URL:** `https://api.hellosign.com/v3`
- **Official documentation:** [Send Signature Request](https://developers.hellosign.com/api/reference/operation/signatureRequestSend/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_urls[]` | body | `array<string>` | no | One or more public file URLs for Dropbox Sign to fetch. Use this or uploaded files, not both. |
| `message` | body | `string` | no | The email message sent to signers. |
| `signers[].email_address` | body | `string` | yes | The email address of the signer. |
| `signers[].name` | body | `string` | yes | The name of the signer. |
| `subject` | body | `string` | no | The email subject sent to signers. |
| `test_mode` | body | `boolean` | no | Whether to create the signature request in test mode. |
| `title` | body | `string` | no | The title to assign to the signature request. |
| `use_text_tags` | body | `boolean` | no | Whether to enable Dropbox Sign text tag parsing in the document. |
