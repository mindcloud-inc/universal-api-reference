# Parsio: Native API Reference

A consolidated summary of Parsio's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://help.parsio.io/public-api/parsio-public-api
- **API base URL:** `https://api.parsio.io`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://help.parsio.io/public-api/parsio-public-api)

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create HTML or Text Document](actions/create-html-or-text-document.md) | `POST /mailboxes/:mailbox_id/doc` | [docs](https://help.parsio.io/public-api/parse-html-and-text-documents-using-api-1) |
| [Create Mailbox](actions/create-mailbox.md) | `POST /mailboxes/create` | [docs](https://help.parsio.io/public-api/parsio-public-api) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks/:mailbox_id` | [docs](https://help.parsio.io/public-api/parsio-public-api) |
| [Delete Mailbox](actions/delete-mailbox.md) | `DELETE /mailboxes/:mailbox_id` | [docs](https://help.parsio.io/public-api/parsio-public-api) |
| [Delete Templates](actions/delete-templates.md) | `DELETE /templates` | [docs](https://help.parsio.io/public-api/parsio-public-api) |
| [Delete Webhooks](actions/delete-webhooks.md) | `DELETE /webhooks` | [docs](https://help.parsio.io/public-api/parsio-public-api) |
| [Disable Templates](actions/disable-templates.md) | `POST /templates/disable_many` | [docs](https://help.parsio.io/public-api/parsio-public-api) |
| [Enable Templates](actions/enable-templates.md) | `POST /templates/enable_many` | [docs](https://help.parsio.io/public-api/parsio-public-api) |
| [Get Document](actions/get-document.md) | `GET /docs/:document_id` | [docs](https://help.parsio.io/public-api/parsio-public-api) |
| [Get Mailbox](actions/get-mailbox.md) | `GET /mailboxes/:mailbox_id` | [docs](https://help.parsio.io/public-api/parsio-public-api) |
| [Get Parsed Data](actions/get-parsed-data.md) | `GET /mailboxes/:mailbox_id/parsed` | [docs](https://help.parsio.io/public-api/parsio-public-api) |
| [Get Template](actions/get-template.md) | `GET /templates/:template_id` | [docs](https://help.parsio.io/public-api/parsio-public-api) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/:webhook_id` | [docs](https://help.parsio.io/public-api/parsio-public-api) |
| [List Collected Emails](actions/list-collected-emails.md) | `GET /mailboxes/:mailbox_id/emails` | [docs](https://help.parsio.io/public-api/parsio-public-api) |
| [List Documents](actions/list-documents.md) | `GET /mailboxes/:mailbox_id/docs` | [docs](https://help.parsio.io/public-api/parsio-public-api) |
| [List Mailboxes](actions/list-mailboxes.md) | `GET /mailboxes` | [docs](https://help.parsio.io/public-api/parsio-public-api) |
| [List Table Fields](actions/list-table-fields.md) | `GET /mailboxes/:mailbox_id/tableFields` | [docs](https://help.parsio.io/public-api/parsio-public-api) |
| [List Templates](actions/list-templates.md) | `GET /mailboxes/:mb_id/templates` | [docs](https://help.parsio.io/public-api/parsio-public-api) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks/mb/:mailbox_id` | [docs](https://help.parsio.io/public-api/parsio-public-api) |
| [Parse Document](actions/parse-document.md) | `POST /docs/:document_id/parse` | [docs](https://help.parsio.io/public-api/parsio-public-api) |
| [Skip Documents](actions/skip-documents.md) | `POST /mailboxes/:mailbox_id/docs/skip` | [docs](https://help.parsio.io/public-api/parsio-public-api) |
| [Update Mailbox](actions/update-mailbox.md) | `POST /mailboxes/:mailbox_id` | [docs](https://help.parsio.io/public-api/parsio-public-api) |
| [Update Webhook](actions/update-webhook.md) | `POST /webhooks` | [docs](https://help.parsio.io/public-api/parsio-public-api) |
| [Upload Document File](actions/upload-document-file.md) | `POST /mailboxes/:mailbox_id/upload` | [docs](https://help.parsio.io/public-api/parse-pdf-and-files-using-api-1) |
