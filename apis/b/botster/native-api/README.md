# Botster: Native API Reference

A consolidated summary of Botster's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://botster.io/info/api-docs
- **API base URL:** `https://botster.io/api/v2`

## Authentication

### API Key

Use your Botster API token from the Settings page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://botster.io/info/api-docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The current page number is read from `page`.

## Pagination

Use `per` in the query string to set the page size (default 50). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Job](actions/archive-job.md) | `POST /jobs/:jobId/archive` | [docs](https://botster.io/info/api-docs) |
| [Delete Job](actions/delete-job.md) | `DELETE /jobs/:jobId` | [docs](https://botster.io/info/api-docs) |
| [Delete Run](actions/delete-run.md) | `DELETE /runs/:runId` | [docs](https://botster.io/info/api-docs) |
| [Get Credits](actions/get-credits.md) | `GET /credits` | [docs](https://botster.io/info/api-docs) |
| [Get Job](actions/get-job.md) | `GET /jobs/:jobId` | [docs](https://botster.io/info/api-docs) |
| [Get Run](actions/get-run.md) | `GET /runs/:runId` | [docs](https://botster.io/info/api-docs) |
| [List Bots](actions/list-bots.md) | `GET /bots` | [docs](https://botster.io/info/api-docs) |
| [List Jobs](actions/list-jobs.md) | `GET /jobs` | [docs](https://botster.io/info/api-docs) |
| [Restart Job](actions/restart-job.md) | `POST /jobs/:jobId/restart` | [docs](https://botster.io/info/api-docs) |
| [Run Bulk DNS Lookup](actions/run-bulk-dns-lookup.md) | `POST /bots/bulk-dns-lookup` | [docs](https://botster.io/bots/bulk-dns-lookup) |
| [Run Bulk Whois Lookup](actions/run-bulk-whois-lookup.md) | `POST /bots/bulk-whois-lookup` | [docs](https://botster.io/bots/bulk-whois-lookup) |
| [Run Company Website Finder](actions/run-company-website-finder.md) | `POST /bots/company-website-finder` | [docs](https://botster.io/bots/company-website-finder) |
| [Run Contact Data Scraper](actions/run-contact-data-scraper.md) | `POST /bots/contact-data-scraper` | [docs](https://botster.io/bots/contact-data-scraper) |
| [Run Find Subdomains](actions/run-find-subdomains.md) | `POST /bots/find-subdomains` | [docs](https://botster.io/bots/find-subdomains) |
| [Run Google Maps Places Scraper](actions/run-google-maps-places-scraper.md) | `POST /bots/google-maps-places-scraper` | [docs](https://botster.io/bots/google-maps-places-scraper) |
| [Run Google Maps Reviews Scraper](actions/run-google-maps-reviews-scraper.md) | `POST /bots/google-maps-reviews-scraper` | [docs](https://botster.io/bots/google-maps-reviews-scraper) |
| [Run Google Pagespeed Bulk Checker](actions/run-google-pagespeed-bulk-checker.md) | `POST /bots/google-pagespeed-bulk-checker` | [docs](https://botster.io/bots/google-pagespeed-bulk-checker) |
| [Run Google Rank Checker](actions/run-google-rank-checker.md) | `POST /bots/google-rank-checker` | [docs](https://botster.io/bots/google-rank-checker) |
| [Run Google Search Scraper](actions/run-google-search-scraper.md) | `POST /bots/google-snippet-scraper` | [docs](https://botster.io/bots/google-snippet-scraper) |
| [Run Google Search Suggestions Scraper](actions/run-google-search-suggestions-scraper.md) | `POST /bots/google-search-suggestions-scraper` | [docs](https://botster.io/bots/google-search-suggestions-scraper) |
| [Run LinkedIn Company Finder](actions/run-linked-in-company-finder.md) | `POST /bots/linkedin-company-finder` | [docs](https://botster.io/bots/linkedin-company-finder) |
| [Run LinkedIn Profile to URL Finder](actions/run-linked-in-profile-to-url-finder.md) | `POST /bots/linkedin-profile-to-url` | [docs](https://botster.io/bots/linkedin-profile-to-url) |
| [Run Search Volume and CPC Finder](actions/run-search-volume-and-cpc-finder.md) | `POST /bots/google-keyword-search-volume` | [docs](https://botster.io/bots/google-keyword-search-volume) |
| [Run TikTok Profile Extractor](actions/run-tik-tok-profile-extractor.md) | `POST /bots/tiktok-profile-extractor` | [docs](https://botster.io/bots/tiktok-profile-extractor) |
| [Run Website Traffic Checker](actions/run-website-traffic-checker.md) | `POST /bots/website-traffic-checker` | [docs](https://botster.io/bots/website-traffic-checker) |
| [Run YouTube Search Scraper](actions/run-you-tube-search-scraper.md) | `POST /bots/youtube-search-scraper` | [docs](https://botster.io/bots/youtube-search-scraper) |
| [Search Bots](actions/search-bots.md) | `GET /bots` | [docs](https://botster.io/info/api-docs) |
| [Unarchive Job](actions/unarchive-job.md) | `POST /jobs/:jobId/unarchive` | [docs](https://botster.io/info/api-docs) |
