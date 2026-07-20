# Create Signature Request with Skribble Sign

Creates a new signature request in Skribble Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/signature-requests`
- **Base URL:** `https://api.skribble.com`
- **Official documentation:** [Create Signature Request](https://api-doc.skribble.com/#4dd248c5-1700-4812-977c-445d492fba5e)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | no | The signature request title. |
| `message` | body | `string` | no | Optional message shown to signers. |
| `content` | body | `string` | no | The base64 encoded PDF content. |
| `content_type` | body | `string` | no | Optional MIME type for the uploaded content. |
| `file_url` | body | `string` | no | Public URL of the PDF to sign instead of uploading content. |
| `document_id` | body | `string` | no | Existing Skribble document ID to sign. |
| `quality` | body | `string` | no | Requested signature quality such as SES or AES. |
| `legislation` | body | `string` | no | Requested legislation such as ZERTES. |
| `signatures[]` | body | `array<object>` | no | Signer objects including emails, sequence, and optional visual signature settings. |
| `write_access[]` | body | `array<string>` | no | Users allowed to add signers later when creating without initial signers. |
| `cc_email_addresses[]` | body | `array<string>` | no | Observer email addresses to notify. |
| `attach_on_success[]` | body | `array<string>` | no | Artifacts to attach automatically after signing succeeds. |
| `creator` | body | `string` | no | Specific business member who should own the signature request. |
| `callback_success_url` | body | `string` | no | Callback URL for successful completion. |
| `callback_update_url` | body | `string` | no | Callback URL for status updates. |
| `callback_error_url` | body | `string` | no | Callback URL for callback or signing errors. |
