# Sign.Plus: Native API Reference

A consolidated summary of Sign.Plus's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://apidoc.sign.plus/get-started/introduction
- **API base URL:** `https://restapi.sign.plus/v2`

## Authentication

### API Key

Use a Sign.Plus personal access token as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://apidoc.sign.plus/guides/setup-your-account)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Envelope Annotation](actions/add-envelope-annotation.md) | `POST /envelope/:envelope_id/annotation` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/add-envelope-annotation) |
| [Add Envelope Document](actions/add-envelope-document.md) | `POST /envelope/:envelope_id/document` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/add-envelope-document) |
| [Add Envelope Signing Steps](actions/add-envelope-signing-steps.md) | `POST /envelope/:envelope_id/signing_steps` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/add-envelope-signing-steps) |
| [Create Envelope](actions/create-envelope.md) | `POST /envelope` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/create-new-envelope) |
| [Create Envelope from Template](actions/create-envelope-from-template.md) | `POST /envelope/from_template/:template_id` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/create-new-envelope-from-template) |
| [Create Template](actions/create-template.md) | `POST /template` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/create-new-template) |
| [Duplicate Envelope](actions/duplicate-envelope.md) | `POST /envelope/:envelope_id/duplicate` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/duplicate-envelope) |
| [Get Envelope](actions/get-envelope.md) | `GET /envelope/:envelope_id` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/get-envelope) |
| [Get Envelope Certificate](actions/get-envelope-certificate.md) | `GET /envelope/:envelope_id/certificate` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/get-envelope-certificate) |
| [Get Envelope Document](actions/get-envelope-document.md) | `GET /envelope/:envelope_id/document/:document_id` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/get-envelope-document) |
| [Get Signed Document](actions/get-signed-document.md) | `GET /envelope/:envelope_id/signed_documents/:document_id` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/get-envelope-signed-document) |
| [Get Template](actions/get-template.md) | `GET /template/:template_id` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/get-template) |
| [List Envelope Annotations](actions/list-envelope-annotations.md) | `GET /envelope/:envelope_id/annotations` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/get-envelope-annotations) |
| [List Envelope Documents](actions/list-envelope-documents.md) | `GET /envelope/:envelope_id/documents` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/get-envelope-documents) |
| [List Envelopes](actions/list-envelopes.md) | `POST /envelopes` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/list-envelopes) |
| [List Signed Documents](actions/list-signed-documents.md) | `GET /envelope/:envelope_id/signed_documents` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/get-envelope-signed_documents) |
| [Rename Envelope](actions/rename-envelope.md) | `PUT /envelope/:envelope_id/rename` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/rename-envelope) |
| [Send Envelope](actions/send-envelope.md) | `POST /envelope/:envelope_id/send` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/send-envelope-for-signature) |
| [Set Envelope Comment](actions/set-envelope-comment.md) | `PUT /envelope/:envelope_id/set_comment` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/set-envelope-comment) |
| [Set Envelope Dynamic Fields](actions/set-envelope-dynamic-fields.md) | `PUT /envelope/:envelope_id/dynamic_fields` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/set-envelope-dynamic-fields) |
| [Set Envelope Expiration Date](actions/set-envelope-expiration-date.md) | `PUT /envelope/:envelope_id/set_expiration_date` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/set-envelope-expiration-date) |
| [Set Envelope Legality Level](actions/set-envelope-legality-level.md) | `PUT /envelope/:envelope_id/set_legality_level` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/set-envelope-legality-level) |
| [Set Envelope Notification](actions/set-envelope-notification.md) | `PUT /envelope/:envelope_id/set_notification` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/set-envelope-notification) |
| [Void Envelope](actions/void-envelope.md) | `PUT /envelope/:envelope_id/void` | [docs](https://apidoc.sign.plus/api-reference/endpoints/signplus/void-envelope) |
