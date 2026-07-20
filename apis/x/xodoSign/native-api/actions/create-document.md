# Create Document with Xodo Sign

Creates a new document in Xodo Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/document`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Create Document](https://eversign.com/api/documentation/methods#create-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | query | `string` | yes | The Xodo Sign business ID that owns the new document. |
| `sandbox` | body | `boolean` | no | Set to 1 to enable sandbox mode for document creation. |
| `is_draft` | body | `boolean` | no | Set to 1 to save the document as a draft. |
| `title` | body | `string` | yes | Title for the document. |
| `message` | body | `string` | no | General document message shown to recipients. |
| `embedded` | body | `boolean` | no | Enable embedded requesting for this document. |
| `use_signer_order` | body | `boolean` | no | Require signers to sign in the configured order. |
| `reminders` | body | `boolean` | no | Enable automatic reminders for the document. |
| `require_all_signers` | body | `boolean` | no | Require all signers to complete the document. |
| `files[]` | body | `array<object>` | yes | Array of file objects to include in the document. |
| `files[].name` | body | `string` | yes | Display name for the uploaded file entry. |
| `files[].file_url` | body | `string` | no | Public URL of the file to upload for this file entry. |
| `files[].file_id` | body | `string` | no | Previously uploaded Xodo Sign file ID for this file entry. |
| `files[].file_base64` | body | `string` | no | Base64-encoded file content for this file entry. |
| `signers[]` | body | `array<object>` | yes | Array of signer objects for the document. |
| `signers[].id` | body | `number` | yes | Unique signer ID for the signer entry. |
| `signers[].name` | body | `string` | yes | Full name of the signer. |
| `signers[].email` | body | `string` | yes | Email address of the signer. |
| `signers[].order` | body | `number` | no | Signing order number when signer order is enabled. |
| `signers[].pin` | body | `string` | no | Optional signer PIN. |
| `signers[].signer_authentication_sms_enabled` | body | `boolean` | no | Enable signer SMS authentication for this signer. |
| `signers[].signer_authentication_phone_number` | body | `string` | no | Phone number used for signer SMS authentication. |
