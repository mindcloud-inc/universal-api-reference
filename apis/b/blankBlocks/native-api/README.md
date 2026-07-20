# BlankBlocks: Native API Reference

A consolidated summary of BlankBlocks's API configuration, with links to official documentation.

- **Official docs:** https://docs.blankblocks.com
- **API base URL:** `https://{siteDomain}/api/site`

## Authentication

### API Key

Connect with a BlankBlocks Website API key and the site domain for the website being managed.

### Credentials

- **API Key:** `apiKey` · required
- **Site Domain:** `siteDomain` · required · BlankBlocks website domain used for the per-site Website API. Enter the domain only, without https:// and without /api/site.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.blankblocks.com/start-here/roadmap)

## API conventions

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100). Use `skip` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.
