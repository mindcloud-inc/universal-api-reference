# Harbour: Native API Reference

A consolidated summary of Harbour's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.harbourshare.com/
- **API base URL:** `https://api.myharbourshare.com/v2`

## Authentication

### API Key

Use your Harbour API key. Harbour requires the key in the shared x-api-key request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.harbourshare.com/v2#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `items`. The total page count is read from `pages`. The current page number is read from `page`.

## Pagination

Use `size` in the query string to set the page size (default 50; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `order_by` in the query string. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Annotate Document](actions/annotate-document.md) | `POST /documents/:document_id/annotate` | [docs](https://developers.harbourshare.com/v2#annotate-document) |
| [Convert Document](actions/convert-document.md) | `POST /documents/:document_id/convert` | [docs](https://developers.harbourshare.com/v2#convert-document) |
| [Convert Document From Base64](actions/convert-document-from-base64.md) | `POST /documents/convert` | [docs](https://developers.harbourshare.com/v2#convert-document) |
| [Create Agreement](actions/create-agreement.md) | `POST https://api.harbourshare.com/v1/agreements` | [docs](https://developers.harbourshare.com/#create-agreement) |
| [Create Agreement Link](actions/create-agreement-link.md) | `POST https://api.harbourshare.com/v1/agreement_links` | [docs](https://developers.harbourshare.com/#create-agreement-link) |
| [Create Document](actions/create-document.md) | `POST /documents` | [docs](https://developers.harbourshare.com/v2#create-document) |
| [Create Insights](actions/create-insights.md) | `POST /insights` | [docs](https://developers.harbourshare.com/v2#create-insights) |
| [Download Agreement](actions/download-agreement.md) | `GET https://api.harbourshare.com/v1/agreements/:agreement_id/download` | [docs](https://developers.harbourshare.com/#download-agreement) |
| [Download Agreement Link](actions/download-agreement-link.md) | `GET https://api.harbourshare.com/v1/agreement_links/:agreement_link_id/download` | [docs](https://developers.harbourshare.com/#download-agreement-link) |
| [Get Agreement](actions/get-agreement.md) | `GET https://api.harbourshare.com/v1/agreements/:agreement_id` | [docs](https://developers.harbourshare.com/#get-agreement-by-id) |
| [Get Agreement Link](actions/get-agreement-link.md) | `GET https://api.harbourshare.com/v1/agreement_links/:agreement_link_id` | [docs](https://developers.harbourshare.com/#get-agreement-link-by-id) |
| [Get Agreement Link Submission](actions/get-agreement-link-submission.md) | `GET https://api.harbourshare.com/v1/agreement_links/:agreement_link_id/submissions/:submission_id` | [docs](https://developers.harbourshare.com/#get-agreement-link-submission) |
| [Get Brand](actions/get-brand.md) | `GET https://api.harbourshare.com/v1/organizations/brands/:brand_id` | [docs](https://developers.harbourshare.com/#get-brand-by-id) |
| [Get Document](actions/get-document.md) | `GET /documents/:document_id` | [docs](https://developers.harbourshare.com/v2#get-document) |
| [Get Folder](actions/get-folder.md) | `GET https://api.harbourshare.com/v1/folders/:folder_id` | [docs](https://developers.harbourshare.com/#get-folder-by-id) |
| [Get Item](actions/get-item.md) | `GET https://api.harbourshare.com/v1/items/:item_id` | [docs](https://developers.harbourshare.com/#get-item-by-id) |
| [List Agreement Link Submissions](actions/list-agreement-link-submissions.md) | `GET https://api.harbourshare.com/v1/agreement_links/:agreement_link_id/submissions` | [docs](https://developers.harbourshare.com/#list-agreement-link-submissions) |
| [List Agreement Links](actions/list-agreement-links.md) | `GET https://api.harbourshare.com/v1/agreement_links` | [docs](https://developers.harbourshare.com/#list-agreement-links) |
| [List Agreements](actions/list-agreements.md) | `GET https://api.harbourshare.com/v1/agreements` | [docs](https://developers.harbourshare.com/#list-agreements) |
| [List Brands](actions/list-brands.md) | `GET https://api.harbourshare.com/v1/organizations/brands` | [docs](https://developers.harbourshare.com/#list-brands) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://developers.harbourshare.com/v2#list-documents) |
| [List Folders](actions/list-folders.md) | `GET https://api.harbourshare.com/v1/folders` | [docs](https://developers.harbourshare.com/#list-folders) |
| [List Items](actions/list-items.md) | `GET https://api.harbourshare.com/v1/items` | [docs](https://developers.harbourshare.com/#list-items) |
| [List Organizations](actions/list-organizations.md) | `GET https://api.harbourshare.com/v1/organizations` | [docs](https://developers.harbourshare.com/#list-organizations) |
