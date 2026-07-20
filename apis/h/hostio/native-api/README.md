# Host.io: Native API Reference

A consolidated summary of Host.io's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://host.io/docs
- **API base URL:** `https://host.io/api`

## Authentication

### API Token

Authenticate Host.io requests with an API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://host.io/docs)

## API conventions

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 0–1000). Use `page` in the query string to choose the page; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Domain DNS Records](actions/get-domain-dns-records.md) | `GET /dns/:domain` | [docs](https://host.io/docs) |
| [Get Domain Full Details](actions/get-domain-full-details.md) | `GET /full/:domain` | [docs](https://host.io/docs) |
| [Get Domain Web Metadata](actions/get-domain-web-metadata.md) | `GET /web/:domain` | [docs](https://host.io/docs) |
| [Get Related Domain Counts](actions/get-related-domain-counts.md) | `GET /related/:domain` | [docs](https://host.io/docs) |
| [List Domains by AdSense ID](actions/list-domains-by-adsense-id.md) | `GET /domains/adsense/:value` | [docs](https://host.io/docs) |
| [List Domains by ASN](actions/list-domains-by-asn.md) | `GET /domains/asn/:value` | [docs](https://host.io/docs) |
| [List Domains by Backlink Target](actions/list-domains-by-backlink-target.md) | `GET /domains/backlinks/:value` | [docs](https://host.io/docs) |
| [List Domains by Email Address](actions/list-domains-by-email-address.md) | `GET /domains/email/:value` | [docs](https://host.io/docs) |
| [List Domains by Facebook Handle](actions/list-domains-by-facebook-handle.md) | `GET /domains/facebook/:value` | [docs](https://host.io/docs) |
| [List Domains by Google Analytics ID](actions/list-domains-by-google-analytics-id.md) | `GET /domains/googleanalytics/:value` | [docs](https://host.io/docs) |
| [List Domains by Google Tag Manager ID](actions/list-domains-by-google-tag-manager-id.md) | `GET /domains/gtm/:value` | [docs](https://host.io/docs) |
| [List Domains by Instagram Handle](actions/list-domains-by-instagram-handle.md) | `GET /domains/instagram/:value` | [docs](https://host.io/docs) |
| [List Domains by IP Address](actions/list-domains-by-ip-address.md) | `GET /domains/ip/:value` | [docs](https://host.io/docs) |
| [List Domains by Mail Server](actions/list-domains-by-mail-server.md) | `GET /domains/mx/:value` | [docs](https://host.io/docs) |
| [List Domains by Name Server](actions/list-domains-by-name-server.md) | `GET /domains/ns/:value` | [docs](https://host.io/docs) |
| [List Domains by Redirect Target](actions/list-domains-by-redirect-target.md) | `GET /domains/redirects/:value` | [docs](https://host.io/docs) |
| [List Domains by Twitter Handle](actions/list-domains-by-twitter-handle.md) | `GET /domains/twitter/:value` | [docs](https://host.io/docs) |
