# Clicksign: Native API Reference

A consolidated summary of Clicksign's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://developers.clicksign.com/reference
- **API base URL:** `https://app.clicksign.com/api/v3`

## Authentication

### Access Token

Authenticate with a Clicksign access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.clicksign.com/docs/primeiros-passos)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.api+json` |
| `Content-Type` | `application/vnd.api+json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `page[size]` in the query string to set the page size (default 20). Use `page[number]` in the query string to choose the page; numbering starts at 1.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Authentication Requirement](actions/create-authentication-requirement.md) | `POST /envelopes/:envelope_id/requirements` | [docs](https://developers.clicksign.com/reference/criar-requisito-de-autenticacao) |
| [Create Bulk Requirements](actions/create-bulk-requirements.md) | `POST /envelopes/:envelope_id/bulk_requirements` | [docs](https://developers.clicksign.com/reference/bulk-requirements) |
| [Create Document](actions/create-document.md) | `POST /envelopes/:envelope_id/documents` | [docs](https://developers.clicksign.com/reference/api-upload-documentos) |
| [Create Envelope](actions/create-envelope.md) | `POST /envelopes` | [docs](https://developers.clicksign.com/reference/api-criar-envelope) |
| [Create Qualification Requirement](actions/create-qualification-requirement.md) | `POST /envelopes/:envelope_id/requirements` | [docs](https://developers.clicksign.com/reference/criar-requisito-qualificacao) |
| [Create Signer](actions/create-signer.md) | `POST /envelopes/:envelope_id/signers` | [docs](https://developers.clicksign.com/reference/api-criar-signatario) |
| [Delete Document](actions/delete-document.md) | `DELETE /envelopes/:envelope_id/documents/:document_id` | [docs](https://developers.clicksign.com/reference/api-excluir-documento) |
| [Delete Envelope](actions/delete-envelope.md) | `DELETE /envelopes/:envelope_id` | [docs](https://developers.clicksign.com/reference/api-excluir-envelope) |
| [Delete Requirement](actions/delete-requirement.md) | `DELETE /envelopes/:envelope_id/requirements/:requirement_id` | [docs](https://developers.clicksign.com/reference/api-excluir-requisito) |
| [Delete Signer](actions/delete-signer.md) | `DELETE /envelopes/:envelope_id/signers/:signer_id` | [docs](https://developers.clicksign.com/reference/api-excluir-signatario) |
| [Get Document](actions/get-document.md) | `GET /envelopes/:envelope_id/documents/:document_id` | [docs](https://developers.clicksign.com/reference/detalhes-do-documento) |
| [Get Envelope](actions/get-envelope.md) | `GET /envelopes/:envelope_id` | [docs](https://developers.clicksign.com/reference/api-detalhes-do-envelope) |
| [Get Requirement](actions/get-requirement.md) | `GET /envelopes/:envelope_id/requirements/:requirement_id` | [docs](https://developers.clicksign.com/reference/detalhes-do-requisito) |
| [Get Signer](actions/get-signer.md) | `GET /envelopes/:envelope_id/signers/:signer_id` | [docs](https://developers.clicksign.com/reference/api-detalhes-do-signatario) |
| [List Document Events](actions/list-document-events.md) | `GET /envelopes/:envelope_id/documents/:document_id/events` | [docs](https://developers.clicksign.com/reference/eventos-de-um-documento) |
| [List Documents](actions/list-documents.md) | `GET /envelopes/:envelope_id/documents` | [docs](https://developers.clicksign.com/reference/api-listar-documentos) |
| [List Envelope Document Events](actions/list-envelope-document-events.md) | `GET /envelopes/:envelope_id/events` | [docs](https://developers.clicksign.com/reference/eventos-do-envelope) |
| [List Envelopes](actions/list-envelopes.md) | `GET /envelopes` | [docs](https://developers.clicksign.com/reference/api-listar-envelopes) |
| [List Requirements](actions/list-requirements.md) | `GET /envelopes/:envelope_id/requirements` | [docs](https://developers.clicksign.com/reference/api-listar-requisitos) |
| [List Signers](actions/list-signers.md) | `GET /envelopes/:envelope_id/signers` | [docs](https://developers.clicksign.com/reference/api-listar-signatarios) |
| [Notify Envelope Signers](actions/notify-envelope-signers.md) | `POST /envelopes/:envelope_id/notifications` | [docs](https://developers.clicksign.com/reference/api-notificar-envelope) |
| [Update Document](actions/update-document.md) | `PATCH /envelopes/:envelope_id/documents/:document_id` | [docs](https://developers.clicksign.com/reference/editar-documento) |
| [Update Envelope](actions/update-envelope.md) | `PATCH /envelopes/:envelope_id` | [docs](https://developers.clicksign.com/reference/api-editar-envelope) |
