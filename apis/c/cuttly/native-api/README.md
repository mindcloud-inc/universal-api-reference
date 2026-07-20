# Cutt.ly: Native API Reference

A consolidated summary of Cutt.ly's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://cutt.ly/cuttly-api
- **API base URL:** `https://cutt.ly/api`

## Authentication

### API Key

Use a Cutt.ly API key. Dedicated Team-generated keys may also work when they authenticate successfully on the regular API endpoint.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://cutt.ly/api-documentation/cuttly-links-api)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Link Tag](actions/add-link-tag.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Change Link Alias](actions/change-link-alias.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Change Source URL](actions/change-source-url.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Delete Link](actions/delete-link.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Get Link Statistics](actions/get-link-statistics.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Get Link Statistics By Date Range](actions/get-link-statistics-by-date-range.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Remove AB/C Test](actions/remove-abc-test.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Remove Expiration](actions/remove-expiration.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Remove Mobile Redirect](actions/remove-mobile-redirect.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Remove Unique Clicks](actions/remove-unique-clicks.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Set AB Test](actions/set-ab-test.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Set ABC Test](actions/set-abc-test.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Set Android Deferred Deep Link](actions/set-android-deferred-deep-link.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Set Click Expiration](actions/set-click-expiration.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Set Date Expiration](actions/set-date-expiration.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Set Link Password](actions/set-link-password.md) | `POST /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Set Link Title](actions/set-link-title.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Set Mobile Redirect](actions/set-mobile-redirect.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Set Unique Clicks](actions/set-unique-clicks.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Set Unique Clicks to 15 Minutes](actions/set-unique-clicks-to15-minutes.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Shorten Link](actions/shorten-link.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Shorten Link With Alias](actions/shorten-link-with-alias.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Shorten Link With Custom Domain](actions/shorten-link-with-custom-domain.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
| [Shorten Link With Public Stats](actions/shorten-link-with-public-stats.md) | `GET /api.php` | [docs](https://cutt.ly/api-documentation/cuttly-links-api) |
