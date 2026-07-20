# Wayback Machine: Native API Reference

A consolidated summary of Wayback Machine's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://archive.org/help/wayback_api.php
- **API base URL:** `https://archive.org`

## Authentication

### No authentication

Public Wayback Machine lookup APIs do not require credentials for the supported read actions.

This API does not require request authentication.

[Official authentication documentation](https://archive.org/help/wayback_api.php)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check URL Availability](actions/check-url-availability.md) | `GET /wayback/available` | [docs](https://archive.org/help/wayback_api.php) |
| [Get CDX Page Count](actions/get-cdx-page-count.md) | `GET https://web.archive.org/cdx/search/cdx` | [docs](https://github.com/internetarchive/wayback/blob/master/wayback-cdx-server/README.md) |
| [Get Closest Capture By Timestamp](actions/get-closest-capture-by-timestamp.md) | `GET /wayback/available` | [docs](https://archive.org/help/wayback_api.php) |
| [Get Latest CDX Capture](actions/get-latest-cdx-capture.md) | `GET https://web.archive.org/cdx/search/cdx` | [docs](https://github.com/internetarchive/wayback/blob/master/wayback-cdx-server/README.md) |
| [Get Oldest CDX Capture](actions/get-oldest-cdx-capture.md) | `GET https://web.archive.org/cdx/search/cdx` | [docs](https://github.com/internetarchive/wayback/blob/master/wayback-cdx-server/README.md) |
| [Search CDX Captures](actions/search-cdx-captures.md) | `GET https://web.archive.org/cdx/search/cdx` | [docs](https://github.com/internetarchive/wayback/blob/master/wayback-cdx-server/README.md) |
