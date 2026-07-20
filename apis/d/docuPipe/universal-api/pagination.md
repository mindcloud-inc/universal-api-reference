# DocuPipe Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model DocuPipe expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/list-analyses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## DocuPipe actions that support pagination

- [List Analyses](actions/list-analyses.md)
- [List Documents](actions/list-documents.md)
- [List Jobs](actions/list-jobs.md)
- [List Reviews](actions/list-reviews.md)
- [List Schemas](actions/list-schemas.md)
- [List Standardizations](actions/list-standardizations.md)
- [Search Documents](actions/search-documents.md)
- [Search Standardizations](actions/search-standardizations.md)
