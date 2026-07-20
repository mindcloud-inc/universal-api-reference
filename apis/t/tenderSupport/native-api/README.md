# Tender Support: Native API Reference

A consolidated summary of Tender Support's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://help.tenderapp.com/kb/api/introduction
- **API base URL:** `https://api.tenderapp.com/help`

## Authentication

### Tender API Token Header

Authenticate to the Tender JSON API by sending the support-site API token in the X-Tender-Auth header.

### Credentials

- **API Key:** `apiKey` · required · The Tender API token from your Tender profile page.

[Official authentication documentation](https://help.tenderapp.com/kb/api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.tender-v1+json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://help.tenderapp.com/kb/api/users) |
| [Get Article](actions/get-article.md) | `GET /faqs/:faqId` | [docs](https://help.tenderapp.com/kb/api/kb-articles) |
| [Get Category](actions/get-category.md) | `GET /categories/:categoryId` | [docs](https://help.tenderapp.com/kb/api/categories) |
| [Get Discussion](actions/get-discussion.md) | `GET /discussions/:discussionId` | [docs](https://help.tenderapp.com/kb/api/discussions) |
| [Get Site](actions/get-site.md) | `GET /` | [docs](https://help.tenderapp.com/kb/api/sites) |
| [List Articles](actions/list-articles.md) | `GET /faqs` | [docs](https://help.tenderapp.com/kb/api/kb-articles) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://help.tenderapp.com/kb/api/categories) |
| [List Discussions](actions/list-discussions.md) | `GET /discussions` | [docs](https://help.tenderapp.com/kb/api/discussions) |
| [List Queue Discussions](actions/list-queue-discussions.md) | `GET /queues/:queueId/discussions` | [docs](https://help.tenderapp.com/kb/api/queues) |
| [List Sections](actions/list-sections.md) | `GET /sections` | [docs](https://help.tenderapp.com/kb/api/sections) |
