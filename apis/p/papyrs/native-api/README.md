# Papyrs: Native API Reference

A consolidated summary of Papyrs's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://papyrs.com/docs/api/
- **API base URL:** `https://{subdomain}.papyrs.com/api/v1`

## Authentication

### API Token

Connect Papyrs with a generated API token and your Papyrs subdomain.

### Credentials

- **API Key:** `apiKey` · required
- **Subdomain:** `subdomain` · required · The Papyrs workspace subdomain used in your Papyrs URL, for example `company` in `https://company.papyrs.com`.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://papyrs.com/docs/api/)

## Pagination

Use `items_per_page` in the query string to set the page size (default 50; accepted range 1–250). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Attachment Widget](actions/create-attachment-widget.md) | `POST /page/:page_id/attachment/create/` | [docs](https://papyrs.com/docs/api/) |
| [Create Heading Widget](actions/create-heading-widget.md) | `POST /page/:page_id/heading/create/` | [docs](https://papyrs.com/docs/api/) |
| [Create Page](actions/create-page.md) | `POST /pages/create/` | [docs](https://papyrs.com/docs/api/) |
| [Create Text Box Widget](actions/create-text-box-widget.md) | `POST /page/:page_id/paragraph/create/` | [docs](https://papyrs.com/docs/api/) |
| [Delete Attachment Widget](actions/delete-attachment-widget.md) | `POST /page/:page_id/attachment/delete/:widget_id/` | [docs](https://papyrs.com/docs/api/) |
| [Delete Heading Widget](actions/delete-heading-widget.md) | `POST /page/:page_id/heading/delete/:widget_id/` | [docs](https://papyrs.com/docs/api/) |
| [Delete Page](actions/delete-page.md) | `POST /pages/delete/:page_id/` | [docs](https://papyrs.com/docs/api/) |
| [Delete Text Box Widget](actions/delete-text-box-widget.md) | `POST /page/:page_id/paragraph/delete/:widget_id/` | [docs](https://papyrs.com/docs/api/) |
| [Delete User](actions/delete-user.md) | `POST /people/delete/:user_id/` | [docs](https://papyrs.com/docs/api/) |
| [Get Attachment Widget](actions/get-attachment-widget.md) | `GET /page/:page_id/attachment/get/:widget_id/` | [docs](https://papyrs.com/docs/api/) |
| [Get Heading Widget](actions/get-heading-widget.md) | `GET /page/:page_id/heading/get/:widget_id/` | [docs](https://papyrs.com/docs/api/) |
| [Get Page](actions/get-page.md) | `GET /pages/get/:page_id/` | [docs](https://papyrs.com/docs/api/) |
| [Get Text Box Widget](actions/get-text-box-widget.md) | `GET /page/:page_id/paragraph/get/:widget_id/` | [docs](https://papyrs.com/docs/api/) |
| [List Page Records](actions/list-page-records.md) | `GET /pages/records/:page_id/` | [docs](https://papyrs.com/docs/api/) |
| [List Pages](actions/list-pages.md) | `GET /pages/all/` | [docs](https://papyrs.com/docs/api/) |
| [List People](actions/list-people.md) | `GET /people/all/` | [docs](https://papyrs.com/docs/api/) |
| [Post To Activity Stream](actions/post-to-activity-stream.md) | `POST /feed/post/` | [docs](https://papyrs.com/docs/api/) |
| [Post To Page Discussion](actions/post-to-page-discussion.md) | `POST /feed/post/:page_id/` | [docs](https://papyrs.com/docs/api/) |
| [Search Results](actions/search-results.md) | `GET /search/query/` | [docs](https://papyrs.com/docs/api/) |
| [Update Attachment Widget](actions/update-attachment-widget.md) | `POST /page/:page_id/attachment/update/:widget_id/` | [docs](https://papyrs.com/docs/api/) |
| [Update Heading Widget](actions/update-heading-widget.md) | `POST /page/:page_id/heading/update/:widget_id/` | [docs](https://papyrs.com/docs/api/) |
| [Update Text Box Widget](actions/update-text-box-widget.md) | `POST /page/:page_id/paragraph/update/:widget_id/` | [docs](https://papyrs.com/docs/api/) |
