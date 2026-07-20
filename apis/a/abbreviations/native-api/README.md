# Abbreviations: Native API Reference

A consolidated summary of Abbreviations's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://www.abbreviations.com/abbr_api.php
- **API base URL:** `https://www.stands4.com/services/v2`

## Authentication

### STANDS4 API Credentials

Authenticate requests with the STANDS4 API user id and developer token id.

### Credentials

- **API User ID:** `uid` · required · STANDS4 API user id required as the `uid` query parameter.
- **Developer Token ID:** `tokenid` · required · STANDS4 developer token id required as the `tokenid` query parameter.

[Official authentication documentation](https://www.abbreviations.com/abbr_api.php)

## API conventions

Response data is read from `result`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Lookup Abbreviation](actions/lookup-abbreviation.md) | `GET /abbr.php` | [docs](https://www.abbreviations.com/abbr_api.php) |
| [Reverse Lookup Abbreviation](actions/reverse-lookup-abbreviation.md) | `GET /abbr.php` | [docs](https://www.abbreviations.com/abbr_api.php) |
