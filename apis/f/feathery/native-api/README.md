# Feathery: Native API Reference

A consolidated summary of Feathery's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.feathery.io/
- **API base URL:** `https://api.feathery.io`

## Authentication

### API Key

Authenticate with a Feathery admin API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api-docs.feathery.io/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Copy a Form](actions/copy-a-form.md) | `POST /api/form/copy/` | [docs](https://api-docs.feathery.io/#copy-a-form) |
| [Create a Form](actions/create-a-form.md) | `POST /api/form/` | [docs](https://api-docs.feathery.io/#create-a-form) |
| [Create and Fetch a User](actions/create-and-fetch-a-user.md) | `POST /api/user/` | [docs](https://api-docs.feathery.io/#create-and-fetch-a-user) |
| [Create Hidden Field](actions/create-hidden-field.md) | `POST /api/form/hidden_field/` | [docs](https://api-docs.feathery.io/#create-hidden-field) |
| [Create or Update Form Submissions](actions/create-or-update-form-submissions.md) | `POST /api/form/submission/` | [docs](https://api-docs.feathery.io/#create-or-update-form-submissions) |
| [Delete a Form](actions/delete-a-form.md) | `DELETE /api/form/:form_id/` | [docs](https://api-docs.feathery.io/#delete-a-form) |
| [Delete a User](actions/delete-a-user.md) | `DELETE /api/user/:id/` | [docs](https://api-docs.feathery.io/#delete-a-user) |
| [Delete Document Envelope](actions/delete-document-envelope.md) | `DELETE /api/document/envelope/:envelope_id/` | [docs](https://api-docs.feathery.io/#delete-document-envelope) |
| [Edit Account](actions/edit-account.md) | `PATCH /api/account/` | [docs](https://api-docs.feathery.io/#edit-account) |
| [Export Form Submission PDF](actions/export-form-submission-pdf.md) | `POST /api/form/submission/pdf/` | [docs](https://api-docs.feathery.io/#export-form-submission-pdf) |
| [Fill or Sign a Document Template](actions/fill-or-sign-a-document-template.md) | `POST /api/document/fill/` | [docs](https://api-docs.feathery.io/#fill-or-sign-a-document-template) |
| [Get User Form Session](actions/get-user-form-session.md) | `GET /api/user/:user_id/session/` | [docs](https://api-docs.feathery.io/#get-user-form-session) |
| [Invite Accounts](actions/invite-accounts.md) | `POST /api/account/invite/` | [docs](https://api-docs.feathery.io/#invite-accounts) |
| [List All Data for a User](actions/list-all-data-for-a-user.md) | `GET /api/field/` | [docs](https://api-docs.feathery.io/#list-all-data-for-a-user) |
| [List All Users](actions/list-all-users.md) | `GET /api/user/` | [docs](https://api-docs.feathery.io/#list-all-users) |
| [List API Connector Errors](actions/list-api-connector-errors.md) | `GET /api/logs/api-connector/:form_id/` | [docs](https://api-docs.feathery.io/#list-api-connector-errors) |
| [List Document Envelopes](actions/list-document-envelopes.md) | `GET /api/document/envelope/` | [docs](https://api-docs.feathery.io/#list-document-envelopes) |
| [List Document Templates](actions/list-document-templates.md) | `GET /api/document/template/` | [docs](https://api-docs.feathery.io/#list-document-templates) |
| [List Email Issues](actions/list-email-issues.md) | `GET /api/logs/email/issues/` | [docs](https://api-docs.feathery.io/#list-email-issues) |
| [List Emails Sent From Form](actions/list-emails-sent-from-form.md) | `GET /api/logs/email/form/:form_id/` | [docs](https://api-docs.feathery.io/#list-emails-sent-from-form) |
| [List Form Submissions](actions/list-form-submissions.md) | `GET /api/form/submission/` | [docs](https://api-docs.feathery.io/#list-form-submissions) |
| [List Forms](actions/list-forms.md) | `GET /api/form/` | [docs](https://api-docs.feathery.io/#list-forms) |
| [List Hidden Fields](actions/list-hidden-fields.md) | `GET /api/form/hidden_field/` | [docs](https://api-docs.feathery.io/#list-hidden-fields) |
| [List Quik Integration Requests](actions/list-quik-integration-requests.md) | `GET /api/logs/quik/:form_id/` | [docs](https://api-docs.feathery.io/#list-quik-integration-requests) |
| [Remove Account](actions/remove-account.md) | `PATCH /api/account/uninvite/` | [docs](https://api-docs.feathery.io/#remove-account) |
| [Retrieve Account Information](actions/retrieve-account-information.md) | `GET /api/account/` | [docs](https://api-docs.feathery.io/#retrieve-account-information) |
| [Retrieve Form Schema](actions/retrieve-form-schema.md) | `GET /api/form/:form_id/` | [docs](https://api-docs.feathery.io/#retrieve-a-form-schema) |
| [Update a Form](actions/update-a-form.md) | `PATCH /api/form/:form_id/` | [docs](https://api-docs.feathery.io/#update-a-form) |
