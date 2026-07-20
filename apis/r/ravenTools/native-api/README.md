# Raven Tools: Native API Reference

A consolidated summary of Raven Tools's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://api.raventools.com/docs/
- **API base URL:** `https://api.raventools.com`

## Authentication

### API Key

Raven Tools API key passed as the required `key` query parameter on every request.

### Credentials

- **API Key:** `apiKey` · optional · Raven Tools API key. Raven requires this value as the `key` query parameter on each request.

[Official authentication documentation](https://raven.zendesk.com/hc/en-us/articles/202177654-How-to-Generate-an-API-Key)

## Retry behavior

Retry responses with status codes `503`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate Link](actions/activate-link.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [Add Domain](actions/add-domain.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [Add Keyword](actions/add-keyword.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [Create Blog Comment Link](actions/create-blog-comment-link.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [Create Competitor Backlink](actions/create-competitor-backlink.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [Create Link](actions/create-link.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [Create Links](actions/create-links.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [Create Organic Link](actions/create-organic-link.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [Create Paid Link](actions/create-paid-link.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [Create Referral Link](actions/create-referral-link.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [Deactivate Link](actions/deactivate-link.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [Decline Link](actions/decline-link.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [Delete Link](actions/delete-link.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [Delete Links](actions/delete-links.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [Get Domain Info](actions/get-domain-info.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [Get Profile Info](actions/get-profile-info.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [List Competitors](actions/list-competitors.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [List Domains](actions/list-domains.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [List Keywords](actions/list-keywords.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [List Keywords With Tags](actions/list-keywords-with-tags.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [List Link Types](actions/list-link-types.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [List Links](actions/list-links.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [List Links By Tag](actions/list-links-by-tag.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [List Website Types](actions/list-website-types.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [Queue Link](actions/queue-link.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [Remove Domain](actions/remove-domain.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [Remove Keyword](actions/remove-keyword.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [Request Link](actions/request-link.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [Update Link](actions/update-link.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [Update Links](actions/update-links.md) | `GET /api` | [docs](https://api.raventools.com/docs/) |
| [Upload Links CSV](actions/upload-links-csv.md) | `POST /api` | [docs](https://api.raventools.com/docs/) |
