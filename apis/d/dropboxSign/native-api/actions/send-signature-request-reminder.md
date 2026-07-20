# Send Signature Request Reminder with Dropbox Sign

Sends a signature request reminder in Dropbox Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/signature_request/remind/:signature_request_id`
- **Base URL:** `https://api.hellosign.com/v3`
- **Official documentation:** [Send Signature Request Reminder](https://developers.hellosign.com/api/reference/operation/signatureRequestRemind/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_address` | body | `string` | yes | The email address of the signer to send a reminder to. |
| `name` | body | `string` | no | The signer name. Include it if two or more signers share an email address. |
| `signature_request_id` | path | `string` | yes | The id of the SignatureRequest to send a reminder for. |
