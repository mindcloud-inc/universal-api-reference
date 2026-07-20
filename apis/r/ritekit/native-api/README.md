# Ritekit: Native API Reference

A consolidated summary of Ritekit's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest
- **API base URL:** `https://api.ritekit.com`

## Authentication

### API Key

Use your Ritekit Client ID access token for authenticated API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.ritekit.com/en/article/general-ritekit-api-faq-legality-changing-tiers-using-multiple-endpoints-etc-1lvapvk/)

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Auto-Emojify Text](actions/auto-emojify-text.md) | `GET /v1/emoji/auto-emojify` | [docs](https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest) |
| [Auto-Hashtag Post](actions/auto-hashtag-post.md) | `GET /v1/stats/auto-hashtag` | [docs](https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest) |
| [Clean Banned Instagram Hashtags](actions/clean-banned-instagram-hashtags.md) | `GET /v2/instagram/hashtags-cleaner` | [docs](https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest) |
| [Detect Disposable Email](actions/detect-disposable-email.md) | `GET /v2/person-insights/disposable-email-detection` | [docs](https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest) |
| [Detect Freemail Address](actions/detect-freemail-address.md) | `GET /v2/person-insights/freemail-detection` | [docs](https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest) |
| [Extract Article From URL](actions/extract-article-from-url.md) | `GET /v2/text/extract-article` | [docs](https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest) |
| [Extract Name From Email](actions/extract-name-from-email.md) | `GET /v2/person-insights/name-from-email-address` | [docs](https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest) |
| [Extract Top Image From URL](actions/extract-top-image-from-url.md) | `GET /v2/image/extract-image` | [docs](https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest) |
| [Get Company Brand Colors](actions/get-company-brand-colors.md) | `GET /v2/company-insights/brand-colors` | [docs](https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest) |
| [Get Company Logo](actions/get-company-logo.md) | `GET /v2/company-insights/logo` | [docs](https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest) |
| [Get Domains From Company Name](actions/get-domains-from-company-name.md) | `GET /v2/company-insights/name-to-domain` | [docs](https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest) |
| [Get Emoji Suggestions](actions/get-emoji-suggestions.md) | `GET /v1/emoji/suggestions` | [docs](https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest) |
| [Get Full Email Insights](actions/get-full-email-insights.md) | `GET /v2/person-insights/full-email-insights` | [docs](https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest) |
| [Get Hashtag Stats](actions/get-hashtag-stats.md) | `GET /v1/stats/multiple-hashtags` | [docs](https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest) |
| [Get Hashtag Suggestions For Image](actions/get-hashtag-suggestions-for-image.md) | `GET /v1/stats/hashtag-suggestions-image` | [docs](https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest) |
| [Get Hashtag Suggestions For Text](actions/get-hashtag-suggestions-for-text.md) | `GET /v1/stats/hashtag-suggestions` | [docs](https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest) |
| [Get Hashtag Suggestions For URL](actions/get-hashtag-suggestions-for-url.md) | `GET /v2/stats/hashtags-for-url` | [docs](https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest) |
| [Get Link Preview](actions/get-link-preview.md) | `GET /v2/text/link-preview` | [docs](https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest) |
| [List Trending Hashtags](actions/list-trending-hashtags.md) | `GET /v1/search/trending` | [docs](https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest) |
| [Suggest Email Typo Fixes](actions/suggest-email-typo-fixes.md) | `GET /v2/person-insights/email-typo` | [docs](https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest) |
