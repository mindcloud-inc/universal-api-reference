# <img src="https://images.mindcloud.co/apps/icons/ar-xiv_1776266428156.png" alt="arXiv logo" width="28" height="28"> arXiv: Universal API

Search and retrieve scholarly paper metadata from the public arXiv API, including articles, authors, categories, submission dates, and feed-level result metadata.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/arXiv/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://arxiv.org
- **Vendor API docs:** https://info.arxiv.org/help/api/user-manual.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Papers](actions/search-papers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/arXiv/latest/actions/search-papers?connectionId=$CONNECTION_ID&limit=25&offset=0&searchQuery=all%3Atransformer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Filter ID List By Search Query](actions/filter-id-list-by-search-query.md) | GET | Finds arXiv papers from an ID list matching a query. |
| [Get Paper By ID](actions/get-paper-by-id.md) | GET | Retrieves a paper from arXiv by ID. |
| [Get Papers By ID List](actions/get-papers-by-id-list.md) | GET | Retrieves papers from arXiv by ID list. |
| [List Recently Submitted Papers](actions/list-recently-submitted-papers.md) | GET | Lists recently submitted papers in arXiv. |
| [List Recently Submitted Papers Ascending](actions/list-recently-submitted-papers-ascending.md) | GET | Lists recently submitted arXiv papers oldest first. |
| [List Recently Updated Papers](actions/list-recently-updated-papers.md) | GET | Lists recently updated papers in arXiv. |
| [List Recently Updated Papers Ascending](actions/list-recently-updated-papers-ascending.md) | GET | Lists recently updated arXiv papers oldest first. |
| [Search Papers](actions/search-papers.md) | GET | Finds papers in arXiv by search query. |
| [Search Papers By Abstract](actions/search-papers-by-abstract.md) | GET | Finds papers in arXiv by abstract. |
| [Search Papers By Author](actions/search-papers-by-author.md) | GET | Finds papers in arXiv by author. |
| [Search Papers By Category](actions/search-papers-by-category.md) | GET | Finds papers in arXiv by category. |
| [Search Papers By Comment](actions/search-papers-by-comment.md) | GET | Finds papers in arXiv by comment. |
| [Search Papers By Identifier](actions/search-papers-by-identifier.md) | GET | Finds papers in arXiv by identifier. |
| [Search Papers By Journal Reference](actions/search-papers-by-journal-reference.md) | GET | Finds papers in arXiv by journal reference. |
| [Search Papers By Relevance Ascending](actions/search-papers-by-relevance-ascending.md) | GET | Finds papers in arXiv by ascending relevance. |
| [Search Papers By Relevance Descending](actions/search-papers-by-relevance-descending.md) | GET | Finds papers in arXiv by descending relevance. |
| [Search Papers By Report Number](actions/search-papers-by-report-number.md) | GET | Finds papers in arXiv by report number. |
| [Search Papers By Title](actions/search-papers-by-title.md) | GET | Finds papers in arXiv by title. |
| [Search Papers With Boolean Query](actions/search-papers-with-boolean-query.md) | GET | Finds papers in arXiv using a Boolean query. |
| [Search Papers With Submitted Date Filter](actions/search-papers-with-submitted-date-filter.md) | GET | Finds papers in arXiv by submitted date range. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Search Papers By Exact Phrase](actions/search-papers-by-exact-phrase.md) | GET | Finds papers in arXiv by exact phrase. |
| [Search Papers With AND Query](actions/search-papers-with-and-query.md) | GET | Finds papers in arXiv using an AND query. |
| [Search Papers With ANDNOT Query](actions/search-papers-with-andnot-query.md) | GET | Finds papers in arXiv using an ANDNOT query. |
| [Search Papers With Grouped Query](actions/search-papers-with-grouped-query.md) | GET | Finds papers in arXiv using a grouped query. |
| [Search Papers With OR Query](actions/search-papers-with-or-query.md) | GET | Finds papers in arXiv using an OR query. |

