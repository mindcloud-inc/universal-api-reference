# Send Signature Request with DigiSigner

Creates a signature request in DigiSigner.

## Endpoint

- **Method:** `POST`
- **Path:** `/signature_requests`
- **Base URL:** `https://api.digisigner.com/v1`
- **Official documentation:** [Send Signature Request](https://www.digisigner.com/esignature-api/esignature-api-documentation/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documents[]` | body | `array<object>` | yes | Array of documents to be signed. Each document includes document_id or template id and its signers. |
| `send_emails` | body | `boolean` | no | Whether DigiSigner sends invitation and notification emails. Defaults to true. |
| `embedded` | body | `boolean` | no | Whether documents are embedded on your website. Defaults to false. |
| `redirect_for_signing_to_url` | body | `string` | no | URL at your website where signers are redirected for signing. |
| `redirect_after_signing_to_url` | body | `string` | no | URL at your website where signers are redirected after signing. |
| `use_text_tags` | body | `boolean` | no | Whether text tags in documents are converted to fields. Defaults to false. |
| `hide_text_tags` | body | `boolean` | no | Whether text tags in documents are hidden. Defaults to false. |
| `send_documents_as_bundle` | body | `boolean` | no | Whether multiple documents should be sent as one bundle. Defaults to false. |
| `bundle_title` | body | `string` | no | Title under which the bundle will be sent to signers. |
| `bundle_subject` | body | `string` | no | Subject of the invitation email for the bundled signature request. |
| `bundle_message` | body | `string` | no | Message of the invitation email for the bundled signature request. |
