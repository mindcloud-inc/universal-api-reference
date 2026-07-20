# Tradeshift: Native API Reference

A consolidated summary of Tradeshift's API configuration, with links to official documentation.

- **Official docs:** https://developers.tradeshift.com/docs/api
- **OpenAPI specification:** https://developers.tradeshift.com/rest/docs/api
- **API base URL:** `https://api.tradeshift.com/tradeshift`

## Authentication

### OAuth1

Connect to Tradeshift with OAuth 1.0 credentials from the API access app and a tenant UUID.

### Credentials

- **Consumer Key:** `consumerKey` · required
- **Consumer Secret:** `consumerSecret` · required
- **Access Token:** `accessToken` · required
- **Token Secret:** `tokenSecret` · required
- **Realm:** `realm` · optional
- **Tenant ID:** `tenantId` · required · Tradeshift tenant/account UUID sent as the X-Tradeshift-TenantId header.

OAuth 1.0a signs every request with the consumer key and secret plus the access token and token secret. Use an OAuth 1.0a client library to construct the `Authorization` header; the signature depends on the HTTP method, URL, and request parameters and should not be assembled as a static token.

[Official authentication documentation](https://support.tradeshift.com/knowledgebase/article/206371144)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. The total page count is read from `numPages`. The current page number is read from `pageId`.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–25). Use `page` in the query string to choose the page; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `contains`, `eq`, `gte`, `lte`.

## Sorting

Set the sort field with `ordering` in the query string. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.
