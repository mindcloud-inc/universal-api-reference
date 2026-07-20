# Create Signature Request with Skribble

Creates a signature request in Skribble.

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
| `attach_on_success[]` | body | `array<string>` | no | Artifacts to attach automatically after signing succeeds. |
| `callback_error_url` | body | `string` | no | Callback URL for callback or signing errors. |
| `callback_success_url` | body | `string` | no | Callback URL for successful completion. |
| `callback_update_url` | body | `string` | no | Callback URL for status updates. |
| `cc_email_addresses[]` | body | `array<string>` | no | Observer email addresses to notify. |
| `content` | body | `string` | no | The base64 encoded PDF content. |
| `content_type` | body | `string` | no | Optional MIME type for the uploaded content. |
| `creator` | body | `string` | no | Specific business member who should own the signature request. |
| `document_id` | body | `string` | no | Existing Skribble document ID to sign. |
| `file_url` | body | `string` | no | Public URL of the PDF to sign instead of uploading content. |
| `legislation` | body | `string` | no | Requested legislation such as ZERTES. |
| `message` | body | `string` | no | Optional message shown to signers. |
| `quality` | body | `string` | no | Requested signature quality such as SES or AES. |
| `signatures[]` | body | `array<object>` | no | Signer objects including emails, sequence, and optional visual signature settings. |
| `title` | body | `string` | no | The signature request title. |
| `write_access[]` | body | `array<string>` | no | Users allowed to add signers later when creating without initial signers. |
