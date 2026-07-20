# Search the Web with Perplexity

Finds web search results in Perplexity by query.

## Endpoint

- **Method:** `POST`
- **Path:** `/search`
- **Base URL:** `https://api.perplexity.ai`
- **Official documentation:** [Search the Web](https://docs.perplexity.ai/api-reference/search-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Search query. Perplexity also accepts an array of queries; this action currently models the common single-query path. |
| `country` | body | `string` | no | ISO 3166-1 alpha-2 country code for geographically relevant results. |
| `max_results` | body | `number` | no | Maximum number of results to return (1-20). |
| `max_tokens` | body | `number` | no | Maximum total tokens of webpage content to return across results. |
| `max_tokens_per_page` | body | `number` | no | Maximum tokens extracted from each webpage. |
| `search_language_filter[]` | body | `array<string>` | no | ISO 639-1 language codes to filter search results. |
| `search_domain_filter[]` | body | `array<string>` | no | Allowlist or denylist of domains to search. |
| `last_updated_after_filter` | body | `string` | no | Return results updated after this date (MM/DD/YYYY). |
| `last_updated_before_filter` | body | `string` | no | Return results updated before this date (MM/DD/YYYY). |
| `search_after_date_filter` | body | `string` | no | Return results published after this date (MM/DD/YYYY). |
| `search_before_date_filter` | body | `string` | no | Return results published before this date (MM/DD/YYYY). |
| `search_recency_filter` | body | `string` | no | Publication recency filter: hour, day, week, month, or year. |
