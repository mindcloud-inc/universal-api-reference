# Adyntel: Native API Reference

A consolidated summary of Adyntel's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://docs.adyntel.com/
- **API base URL:** `https://api.adyntel.com`

## Authentication

### Body API Key

Adyntel authentication sends api_key and email in the request body on every request.

### Credentials

- **API Key:** `apiKey` · required
- **Email:** `email` · required

[Official authentication documentation](https://docs.adyntel.com/authorization)

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Domain Keywords](actions/get-domain-keywords.md) | `POST /domain-keywords` | [docs](https://docs.adyntel.com/ad-libraries/paid-vs-organic-keywords) |
| [Get Google Shopping Status](actions/get-google-shopping-status.md) | `POST /google_shopping_status` | [docs](https://docs.adyntel.com/ad-libraries/google-shopping-status) |
| [Get TikTok Ad Details](actions/get-tik-tok-ad-details.md) | `POST /tiktok_ad_details` | [docs](https://docs.adyntel.com/ad-libraries/tiktok-ad-details) |
| [List Facebook and Instagram Ads](actions/list-facebook-and-instagram-ads.md) | `POST /facebook` | [docs](https://docs.adyntel.com/ad-libraries/meta) |
| [List Google Ads](actions/list-google-ads.md) | `POST /google` | [docs](https://docs.adyntel.com/ad-libraries/google) |
| [List Google Shopping Ads](actions/list-google-shopping-ads.md) | `POST /google_shopping` | [docs](https://docs.adyntel.com/ad-libraries/google-shopping) |
| [List LinkedIn Ads](actions/list-linked-in-ads.md) | `POST /linkedin` | [docs](https://docs.adyntel.com/ad-libraries/linkedin) |
| [Search LinkedIn Ads by Keyword](actions/search-linked-in-ads-by-keyword.md) | `POST /linkedin-keyword-search` | [docs](https://docs.adyntel.com/ad-libraries/linkedin-keyword-search) |
| [Search Meta Ads by Keyword](actions/search-meta-ads-by-keyword.md) | `POST /facebook_ad_search` | [docs](https://docs.adyntel.com/ad-libraries/meta-ad-search) |
| [Search TikTok Ads](actions/search-tik-tok-ads.md) | `POST /tiktok_search` | [docs](https://docs.adyntel.com/ad-libraries/tiktok-search) |
