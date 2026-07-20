# Paperless: Native API Reference

A consolidated summary of Paperless's API configuration and 38 documented operations, with links to official documentation.

- **Official docs:** https://developers.paperless.io/docs/api/f935d3abd73dd-getting-started-with-the-paperless-api
- **API base URL:** `https://app.paperless.io/api/v1`

## Authentication

### Paperless API Key

Use a Paperless integration API key. MindCloud sends it as Authorization: Bearer <apiKey>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.paperless.io/docs/api/f935d3abd73dd-getting-started-with-the-paperless-api)

## API conventions

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace` | query | `string` | no | Paperless workspace ID. |

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (38 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Advanced Document](actions/create-advanced-document.md) | `POST /documents` | [docs](https://developers.paperless.io/docs/api/dbf7092010e15-advanced-document-creation) |
| [Create Blob](actions/create-blob.md) | `POST /blobs` | [docs](https://developers.paperless.io/docs/api/bb191806bdd25-create-a-document-from-a-pdf) |
| [Create Blob For Attachment](actions/create-blob-for-attachment.md) | `POST /blobs` | [docs](https://developers.paperless.io/docs/api/bb191806bdd25-create-a-document-from-a-pdf) |
| [Create Blob For Image](actions/create-blob-for-image.md) | `POST /blobs` | [docs](https://developers.paperless.io/docs/api/bb191806bdd25-create-a-document-from-a-pdf) |
| [Create Blob For PDF](actions/create-blob-for-pdf.md) | `POST /blobs` | [docs](https://developers.paperless.io/docs/api/bb191806bdd25-create-a-document-from-a-pdf) |
| [Create Document](actions/create-document.md) | `POST /documents` | [docs](https://developers.paperless.io/docs/api/529adde2f023e-create-and-send-your-first-document) |
| [Create Document Created Webhook](actions/create-document-created-webhook.md) | `POST /webhooks` | [docs](https://developers.paperless.io/docs/api/1574d17775d21-receive-data-from-document-events-in-real-time-with-webhook-subscriptions) |
| [Create Document From PDF](actions/create-document-from-pdf.md) | `POST /documents` | [docs](https://developers.paperless.io/docs/api/bb191806bdd25-create-a-document-from-a-pdf) |
| [Create Document From Template](actions/create-document-from-template.md) | `POST /documents` | [docs](https://developers.paperless.io/docs/api/95ee69b4b848f-using-templates-with-the-api) |
| [Create Document Updated Webhook](actions/create-document-updated-webhook.md) | `POST /webhooks` | [docs](https://developers.paperless.io/docs/api/1574d17775d21-receive-data-from-document-events-in-real-time-with-webhook-subscriptions) |
| [Create Document With Email Content](actions/create-document-with-email-content.md) | `POST /documents` | [docs](https://developers.paperless.io/docs/api/ec1d64419e849-setting-the-e-mail-content) |
| [Create Document With Form Fields](actions/create-document-with-form-fields.md) | `POST /documents` | [docs](https://developers.paperless.io/docs/api/529adde2f023e-create-and-send-your-first-document) |
| [Create Document With Hidden Blocks](actions/create-document-with-hidden-blocks.md) | `POST /documents` | [docs](https://developers.paperless.io/docs/api/2ba41f7dfe8a3-visibility-of-blocks) |
| [Create Document With Redirect URL](actions/create-document-with-redirect-url.md) | `POST /documents` | [docs](https://developers.paperless.io/docs/api/529adde2f023e-create-and-send-your-first-document) |
| [Create Document With Reminder Settings](actions/create-document-with-reminder-settings.md) | `POST /documents` | [docs](https://developers.paperless.io/docs/api/dbf7092010e15-advanced-document-creation) |
| [Create Document With Signature Fields](actions/create-document-with-signature-fields.md) | `POST /documents` | [docs](https://developers.paperless.io/docs/api/529adde2f023e-create-and-send-your-first-document) |
| [Create Document With Variables](actions/create-document-with-variables.md) | `POST /documents` | [docs](https://developers.paperless.io/docs/api/529adde2f023e-create-and-send-your-first-document) |
| [Create Document With Visible Blocks](actions/create-document-with-visible-blocks.md) | `POST /documents` | [docs](https://developers.paperless.io/docs/api/2ba41f7dfe8a3-visibility-of-blocks) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://developers.paperless.io/docs/api/1574d17775d21-receive-data-from-document-events-in-real-time-with-webhook-subscriptions) |
| [Delete Document](actions/delete-document.md) | `DELETE /documents/:id` | [docs](https://developers.paperless.io/docs/api/529adde2f023e-create-and-send-your-first-document) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:id` | [docs](https://developers.paperless.io/docs/api/1574d17775d21-receive-data-from-document-events-in-real-time-with-webhook-subscriptions) |
| [Get Document](actions/get-document.md) | `GET /documents/:id` | [docs](https://developers.paperless.io/docs/api/529adde2f023e-create-and-send-your-first-document) |
| [Get Submission](actions/get-submission.md) | `GET /submissions/:id` | [docs](https://developers.paperless.io/docs/api/529adde2f023e-create-and-send-your-first-document) |
| [Get Template](actions/get-template.md) | `GET /templates/:id` | [docs](https://developers.paperless.io/docs/api/95ee69b4b848f-using-templates-with-the-api) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/:id` | [docs](https://developers.paperless.io/docs/api/1574d17775d21-receive-data-from-document-events-in-real-time-with-webhook-subscriptions) |
| [List Document Created Webhooks](actions/list-document-created-webhooks.md) | `GET /webhooks` | [docs](https://developers.paperless.io/docs/api/1574d17775d21-receive-data-from-document-events-in-real-time-with-webhook-subscriptions) |
| [List Document Updated Webhooks](actions/list-document-updated-webhooks.md) | `GET /webhooks` | [docs](https://developers.paperless.io/docs/api/1574d17775d21-receive-data-from-document-events-in-real-time-with-webhook-subscriptions) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://developers.paperless.io/docs/api/529adde2f023e-create-and-send-your-first-document) |
| [List Submissions](actions/list-submissions.md) | `GET /submissions` | [docs](https://developers.paperless.io/docs/api/529adde2f023e-create-and-send-your-first-document) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://developers.paperless.io/docs/api/95ee69b4b848f-using-templates-with-the-api) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://developers.paperless.io/docs/api/1574d17775d21-receive-data-from-document-events-in-real-time-with-webhook-subscriptions) |
| [List Webhooks By Event](actions/list-webhooks-by-event.md) | `GET /webhooks` | [docs](https://developers.paperless.io/docs/api/1574d17775d21-receive-data-from-document-events-in-real-time-with-webhook-subscriptions) |
| [Set Document Email Content](actions/set-document-email-content.md) | `PATCH /documents/:id` | [docs](https://developers.paperless.io/docs/api/ec1d64419e849-setting-the-e-mail-content) |
| [Update Document](actions/update-document.md) | `PATCH /documents/:id` | [docs](https://developers.paperless.io/docs/api/dbf7092010e15-advanced-document-creation) |
| [Update Document Block Visibility](actions/update-document-block-visibility.md) | `PATCH /documents/:id` | [docs](https://developers.paperless.io/docs/api/2ba41f7dfe8a3-visibility-of-blocks) |
| [Update Document Created Webhook](actions/update-document-created-webhook.md) | `PATCH /webhooks/:id` | [docs](https://developers.paperless.io/docs/api/1574d17775d21-receive-data-from-document-events-in-real-time-with-webhook-subscriptions) |
| [Update Document Updated Webhook](actions/update-document-updated-webhook.md) | `PATCH /webhooks/:id` | [docs](https://developers.paperless.io/docs/api/1574d17775d21-receive-data-from-document-events-in-real-time-with-webhook-subscriptions) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /webhooks/:id` | [docs](https://developers.paperless.io/docs/api/1574d17775d21-receive-data-from-document-events-in-real-time-with-webhook-subscriptions) |
