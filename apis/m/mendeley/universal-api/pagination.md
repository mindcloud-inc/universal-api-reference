# Mendeley Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Mendeley expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/list-annotations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Mendeley actions that support pagination

- [List Annotations](actions/list-annotations.md)
- [List BibTeX Documents](actions/list-bibtex-documents.md)
- [List Documents](actions/list-documents-stage3.md)
- [List Folders](actions/list-folders.md)
- [List Trashed Documents](actions/list-trashed-documents.md)
