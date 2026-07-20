# Fluxguard: Native API Reference

A consolidated summary of Fluxguard's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://fluxguard.com/how-to-guides/use-our-api/
- **API base URL:** `https://api.fluxguard.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required · Fluxguard API key used for the x-api-key request header.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://fluxguard.com/how-to-guides/use-our-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Page](actions/add-page.md) | `POST /add-page` | [docs](https://fluxguard.com/how-to-guides/use-our-api/) |
| [Create Site Category](actions/create-site-category.md) | `POST /account/category` | [docs](https://fluxguard.com/how-to-guides/use-our-api/) |
| [Create Webhook](actions/create-webhook.md) | `PUT /account/webhook` | [docs](https://fluxguard.com/how-to-guides/use-our-api/) |
| [Delete Page](actions/delete-page.md) | `DELETE /site/:siteId/session/:sessionId/page/:pageId` | [docs](https://fluxguard.com/how-to-guides/use-our-api/) |
| [Delete Site](actions/delete-site.md) | `DELETE /site/:siteId` | [docs](https://fluxguard.com/how-to-guides/use-our-api/) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /account/webhook` | [docs](https://fluxguard.com/how-to-guides/use-our-api/) |
| [Get Account Data](actions/get-account-data.md) | `GET /account` | [docs](https://fluxguard.com/how-to-guides/use-our-api/) |
| [Get Page Data](actions/get-page-data.md) | `GET /site/:siteId/session/:sessionId/page/:pageId` | [docs](https://fluxguard.com/how-to-guides/use-our-api/) |
| [Get Sample Webhook](actions/get-sample-webhook.md) | `GET /account/webhook/sample` | [docs](https://fluxguard.com/how-to-guides/use-our-api/) |
| [Initiate Crawl](actions/initiate-crawl.md) | `POST /site/:siteId/session/:sessionId/crawl` | [docs](https://fluxguard.com/how-to-guides/use-our-api/) |
| [List Categories](actions/list-categories.md) | `GET /account/category` | [docs](https://fluxguard.com/how-to-guides/use-our-api/) |
| [List Webhooks](actions/list-webhooks.md) | `GET /account/webhook` | [docs](https://fluxguard.com/how-to-guides/use-our-api/) |
