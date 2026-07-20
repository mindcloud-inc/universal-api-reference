# Column Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Column expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/column/latest/actions/list-ach-transfers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Column actions that support pagination

- [List ACH Transfers](actions/list-ach-transfers.md)
- [List All Transfers](actions/list-all-transfers.md)
- [List Book Transfers](actions/list-book-transfers.md)
- [List Financial Institutions](actions/list-financial-institutions.md)
- [List Wire Transfers](actions/list-wire-transfers.md)
