# Moaform: Native API Reference

A consolidated summary of Moaform's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://help.moaform.com/hc/en-us/sections/28248280913561-API
- **API base URL:** `https://api.moaform.com/v1`

## Authentication

### API Key

Use a Moaform API key to call the Moaform API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.moaform.com/hc/en-us/articles/28281646661401-API-Key-Creation-and-Management)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `page_size` in the query string to set the page size (default 25; maximum 1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `order_by`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | `POST /forms/:formId/webhooks` | [docs](https://help.moaform.com/hc/en-us/articles/28335977118745-Create-a-New-Webhook) |
| [Delete Response](actions/delete-response.md) | `DELETE /forms/:formId/responses/:responseId` | [docs](https://help.moaform.com/hc/en-us/articles/28407769469209-Deleting-Response) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /forms/:formId/webhooks/:webhookId` | [docs](https://help.moaform.com/hc/en-us/articles/28337019205529-Deleting-Webhook) |
| [Download Submitted Attachment](actions/download-submitted-attachment.md) | `GET /forms/:formId/responses/:responseId/files/:fileId` | [docs](https://help.moaform.com/hc/en-us/articles/28408037219609-Downlodading-Submitted-Attachment) |
| [Get Form](actions/get-form.md) | `GET /forms/:formId` | [docs](https://help.moaform.com/hc/en-us/articles/28407590441241-Fetching-Form-Details) |
| [List Form Responses](actions/list-form-responses.md) | `GET /forms/:formId/responses` | [docs](https://help.moaform.com/hc/en-us/articles/28407667571097-Fetching-Form-Responses) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://help.moaform.com/hc/en-us/articles/28291726457497-Fetching-Form-List) |
| [List Webhooks](actions/list-webhooks.md) | `GET /forms/:formId/webhooks` | [docs](https://help.moaform.com/hc/en-us/articles/28408524240537-Fetching-Webhook-Information) |
| [Update Webhook](actions/update-webhook.md) | `PUT /forms/:formId/webhooks/:webhookId` | [docs](https://help.moaform.com/hc/en-us/articles/28336903807897-Changing-Webhook-Settings) |
