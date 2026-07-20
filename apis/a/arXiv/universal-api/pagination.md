# arXiv Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model arXiv expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/arXiv/latest/actions/list-recently-submitted-papers?connectionId=$CONNECTION_ID&limit=25&offset=0&searchQuery=all%3Atransformer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## arXiv actions that support pagination

- [List Recently Submitted Papers](actions/list-recently-submitted-papers.md)
- [List Recently Submitted Papers Ascending](actions/list-recently-submitted-papers-ascending.md)
- [List Recently Updated Papers](actions/list-recently-updated-papers.md)
- [List Recently Updated Papers Ascending](actions/list-recently-updated-papers-ascending.md)
- [Search Papers](actions/search-papers.md)
- [Search Papers By Abstract](actions/search-papers-by-abstract.md)
- [Search Papers By Author](actions/search-papers-by-author.md)
- [Search Papers By Category](actions/search-papers-by-category.md)
- [Search Papers By Comment](actions/search-papers-by-comment.md)
- [Search Papers By Identifier](actions/search-papers-by-identifier.md)
- [Search Papers By Journal Reference](actions/search-papers-by-journal-reference.md)
- [Search Papers By Relevance Ascending](actions/search-papers-by-relevance-ascending.md)
- [Search Papers By Relevance Descending](actions/search-papers-by-relevance-descending.md)
- [Search Papers By Report Number](actions/search-papers-by-report-number.md)
- [Search Papers By Title](actions/search-papers-by-title.md)
- [Search Papers With Boolean Query](actions/search-papers-with-boolean-query.md)
- [Search Papers With Submitted Date Filter](actions/search-papers-with-submitted-date-filter.md)
