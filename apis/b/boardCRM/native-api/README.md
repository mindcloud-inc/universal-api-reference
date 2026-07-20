# BoardCRM: Native API Reference

A consolidated summary of BoardCRM's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://dev.boardcrm.io/
- **API base URL:** `https://api.boardcrm.io/api`

## Authentication

### API Key

Connect with a BoardCRM board API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://dev.boardcrm.io/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the request body to set the page size. Use `page` in the request body to choose the page; numbering starts at 1.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Change Deal Column](actions/change-deal-column.md) | `POST /offer/change-column` | [docs](https://dev.boardcrm.io/public/0.1/methods/offer#change-column) |
| [Create Deal](actions/create-deal.md) | `POST /offer/create` | [docs](https://dev.boardcrm.io/public/0.1/methods/offer#create) |
| [Create Deal Comment](actions/create-deal-comment.md) | `POST /comment/create` | [docs](https://dev.boardcrm.io/public/0.1/methods/comment#create) |
| [Create Deal Field](actions/create-deal-field.md) | `POST /field/create` | [docs](https://dev.boardcrm.io/public/0.1/methods/field#create) |
| [Create Deals Batch](actions/create-deals-batch.md) | `POST /offer/create-some` | [docs](https://dev.boardcrm.io/public/0.1/methods/offer#create-some) |
| [Delete Deal](actions/delete-deal.md) | `POST /offer/delete` | [docs](https://dev.boardcrm.io/public/0.1/methods/offer#delete) |
| [Delete Deal Field](actions/delete-deal-field.md) | `POST /field/delete` | [docs](https://dev.boardcrm.io/public/0.1/methods/field#delete) |
| [Delete Deals Batch](actions/delete-deals-batch.md) | `POST /offer/delete-some` | [docs](https://dev.boardcrm.io/public/0.1/methods/offer#delete-some) |
| [Delete Lead](actions/delete-lead.md) | `POST /lead/delete` | [docs](https://dev.boardcrm.io/public/0.1/methods/lead#delete) |
| [Export Deals](actions/export-deals.md) | `POST /offer/export` | [docs](https://dev.boardcrm.io/public/0.1/methods/offer#export) |
| [Export Leads](actions/export-leads.md) | `POST /lead/export` | [docs](https://dev.boardcrm.io/public/0.1/methods/lead#export) |
| [Get Deal](actions/get-deal.md) | `POST /offer/get` | [docs](https://dev.boardcrm.io/public/0.1/methods/offer#get) |
| [Get Lead](actions/get-lead.md) | `POST /lead/get` | [docs](https://dev.boardcrm.io/public/0.1/methods/lead#get) |
| [List Deal Fields](actions/list-deal-fields.md) | `POST /field/list` | [docs](https://dev.boardcrm.io/public/0.1/methods/field#list) |
| [List Leads](actions/list-leads.md) | `POST /lead/list` | [docs](https://dev.boardcrm.io/public/0.1/methods/lead#list) |
| [Set Deal Field Values](actions/set-deal-field-values.md) | `POST /offer/set-values` | [docs](https://dev.boardcrm.io/public/0.1/methods/offer#set-values) |
| [Update Deal](actions/update-deal.md) | `POST /offer/update` | [docs](https://dev.boardcrm.io/public/0.1/methods/offer#update) |
| [Update Deal Field](actions/update-deal-field.md) | `POST /field/update` | [docs](https://dev.boardcrm.io/public/0.1/methods/field#update) |
| [Update Lead](actions/update-lead.md) | `POST /lead/update` | [docs](https://dev.boardcrm.io/public/0.1/methods/lead#update) |
