# Piloterr: Native API Reference

A consolidated summary of Piloterr's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://docs.piloterr.com
- **API base URL:** `https://api.piloterr.com/v2`

## Authentication

### API Key

Authenticate Piloterr requests with an API key sent in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required · Your active Piloterr API key.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.piloterr.com/v2/authentication)

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Analyze Email Domain](actions/analyze-email-domain.md) | `GET /email/analyzes` | [docs](https://docs.piloterr.com/email-analyzes) |
| [Check Domain DNSBL](actions/check-domain-dnsbl.md) | `GET /domain/dnsbl` | [docs](https://docs.piloterr.com/domain-dnsbl) |
| [Check Domain Malicious](actions/check-domain-malicious.md) | `GET /domain/malicious` | [docs](https://docs.piloterr.com/domain-malicious) |
| [Count LinkedIn Jobs](actions/count-linkedin-jobs.md) | `GET /linkedin/job/count` | [docs](https://docs.piloterr.com/linkedin-job-count) |
| [Detect Website Technologies](actions/detect-website-technologies.md) | `GET /website/technology` | [docs](https://docs.piloterr.com/website-technology) |
| [Find Professional Email](actions/find-professional-email.md) | `GET /email/finder` | [docs](https://docs.piloterr.com/email-finder) |
| [Get Crunchbase Company Info](actions/get-crunchbase-company-info.md) | `GET /crunchbase/company/info` | [docs](https://docs.piloterr.com/crunchbase-company-info) |
| [Get Crunchbase Funding Round](actions/get-crunchbase-funding-round.md) | `GET /crunchbase/funding_round` | [docs](https://docs.piloterr.com/crunchbase-funding-round) |
| [Get Crunchbase People Info](actions/get-crunchbase-people-info.md) | `GET /crunchbase/people/info` | [docs](https://docs.piloterr.com/crunchbase-people-info) |
| [Get Google Search Autocomplete](actions/get-google-search-autocomplete.md) | `GET /google/search/autocomplete` | [docs](https://docs.piloterr.com/google-search-autocomplete) |
| [Get LinkedIn Company Info](actions/get-linkedin-company-info.md) | `GET /linkedin/company/info` | [docs](https://docs.piloterr.com/linkedin-company-info) |
| [Get LinkedIn Job Info](actions/get-linkedin-job-info.md) | `GET /linkedin/job/info` | [docs](https://docs.piloterr.com/linkedin-job-info) |
| [Get LinkedIn Post Info](actions/get-linkedin-post-info.md) | `GET /linkedin/post/info` | [docs](https://docs.piloterr.com/linkedin-post-info) |
| [Get LinkedIn Product Info](actions/get-linkedin-product-info.md) | `GET /linkedin/product/info` | [docs](https://docs.piloterr.com/linkedin-product-info) |
| [Get LinkedIn Profile Info](actions/get-linkedin-profile-info.md) | `GET /linkedin/profile/info` | [docs](https://docs.piloterr.com/linkedin-profile-info) |
| [Get Owler Company Info](actions/get-owler-company-info.md) | `GET /owler/company/info` | [docs](https://docs.piloterr.com/owler-company-info) |
| [Get Similarweb Domain](actions/get-similarweb-domain.md) | `GET /similarweb/domain` | [docs](https://docs.piloterr.com/similarweb-domain) |
| [Get Trustpilot Company Info](actions/get-trustpilot-company-info.md) | `GET /trustpilot/company/info` | [docs](https://docs.piloterr.com/trustpilot-company-info) |
| [Get Usage](actions/get-usage.md) | `GET /usage` | [docs](https://docs.piloterr.com/usage) |
| [List Crunchbase Funding Rounds](actions/list-crunchbase-funding-rounds.md) | `GET /crunchbase/funding_rounds` | [docs](https://docs.piloterr.com/crunchbase-funding-rounds) |
| [Lookup Domain Whois](actions/lookup-domain-whois.md) | `GET /domain/whois` | [docs](https://docs.piloterr.com/domain-whois) |
| [Search Bing](actions/search-bing.md) | `GET /bing/search` | [docs](https://docs.piloterr.com/bing-search) |
| [Search Brave](actions/search-brave.md) | `GET /brave/search` | [docs](https://docs.piloterr.com/brave-search) |
| [Search Crunchbase](actions/search-crunchbase.md) | `GET /crunchbase/search` | [docs](https://docs.piloterr.com/crunchbase-search) |
| [Search Google](actions/search-google.md) | `GET /google/search` | [docs](https://docs.piloterr.com/google-search) |
| [Search Google Images](actions/search-google-images.md) | `GET /google/images` | [docs](https://docs.piloterr.com/google-images) |
| [Search Google Jobs](actions/search-google-jobs.md) | `GET /google/jobs` | [docs](https://docs.piloterr.com/google-jobs) |
| [Search Google News](actions/search-google-news.md) | `GET /google/news` | [docs](https://docs.piloterr.com/google-news) |
| [Search Google Videos](actions/search-google-videos.md) | `GET /google/videos` | [docs](https://docs.piloterr.com/google-videos) |
| [Search LinkedIn Jobs](actions/search-linkedin-jobs.md) | `GET /linkedin/job/search` | [docs](https://docs.piloterr.com/linkedin-job-search) |
| [Search Owler Companies](actions/search-owler-companies.md) | `GET /owler/search` | [docs](https://docs.piloterr.com/owler-search) |
| [Search Similarweb](actions/search-similarweb.md) | `GET /similarweb/search` | [docs](https://docs.piloterr.com/similarweb-search) |
| [Verify Email Address](actions/verify-email-address.md) | `GET /email/verify` | [docs](https://docs.piloterr.com/email-verify) |
