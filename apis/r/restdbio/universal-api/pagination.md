# Restdb.io Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Restdb.io expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/list-documents?connectionId=$CONNECTION_ID&limit=25&offset=0&collection=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Restdb.io actions that support pagination

- [List Documents](actions/list-documents.md)
- [List Documents Flattened](actions/list-documents-flattened.md)
- [List Documents With Children](actions/list-documents-with-children.md)
- [List Documents With Linked References](actions/list-documents-with-linked-references.md)
- [List Documents With Media Data](actions/list-documents-with-media-data.md)
- [List Documents With Meta Fields](actions/list-documents-with-meta-fields.md)
- [List Documents With Totals](actions/list-documents-with-totals.md)
- [Search Documents](actions/search-documents.md)
