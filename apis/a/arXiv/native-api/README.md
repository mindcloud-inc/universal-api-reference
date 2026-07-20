# arXiv: Native API Reference

A consolidated summary of arXiv's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://info.arxiv.org/help/api/user-manual.html
- **API base URL:** `https://export.arxiv.org/api`

## Authentication

### No Authentication

The public arXiv API does not require credentials for query requests.

This API does not require request authentication.

[Official authentication documentation](https://info.arxiv.org/help/api/basics.html)

## API conventions

Responses from this API use XML.

## Pagination

Use `max_results` in the query string to set the page size (default 10; accepted range 1–2000). Use `start` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sortBy` in the query string. Set the direction separately with `sortOrder`. Use `ascending` for ascending order and `descending` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Filter ID List By Search Query](actions/filter-id-list-by-search-query.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [Get Paper By ID](actions/get-paper-by-id.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [Get Papers By ID List](actions/get-papers-by-id-list.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [List Recently Submitted Papers](actions/list-recently-submitted-papers.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [List Recently Submitted Papers Ascending](actions/list-recently-submitted-papers-ascending.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [List Recently Updated Papers](actions/list-recently-updated-papers.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [List Recently Updated Papers Ascending](actions/list-recently-updated-papers-ascending.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [Search Papers](actions/search-papers.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [Search Papers By Abstract](actions/search-papers-by-abstract.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [Search Papers By Author](actions/search-papers-by-author.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [Search Papers By Category](actions/search-papers-by-category.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [Search Papers By Comment](actions/search-papers-by-comment.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [Search Papers By Exact Phrase](actions/search-papers-by-exact-phrase.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [Search Papers By Identifier](actions/search-papers-by-identifier.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [Search Papers By Journal Reference](actions/search-papers-by-journal-reference.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [Search Papers By Relevance Ascending](actions/search-papers-by-relevance-ascending.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [Search Papers By Relevance Descending](actions/search-papers-by-relevance-descending.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [Search Papers By Report Number](actions/search-papers-by-report-number.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [Search Papers By Title](actions/search-papers-by-title.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [Search Papers With AND Query](actions/search-papers-with-and-query.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [Search Papers With ANDNOT Query](actions/search-papers-with-andnot-query.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [Search Papers With Boolean Query](actions/search-papers-with-boolean-query.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [Search Papers With Grouped Query](actions/search-papers-with-grouped-query.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [Search Papers With OR Query](actions/search-papers-with-or-query.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
| [Search Papers With Submitted Date Filter](actions/search-papers-with-submitted-date-filter.md) | `GET /query` | [docs](https://info.arxiv.org/help/api/user-manual.html) |
