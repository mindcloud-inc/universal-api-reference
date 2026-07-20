# Better Proposals Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Better Proposals expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-custom-merge-tags?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Better Proposals actions that support pagination

- [Get Custom Merge Tags](actions/get-custom-merge-tags.md)
- [List Companies](actions/list-companies.md)
- [List Currencies](actions/list-currencies.md)
- [List Document Types](actions/list-document-types.md)
- [List New Proposals](actions/list-new-proposals.md)
- [List Opened Proposals](actions/list-opened-proposals.md)
- [List Proposals](actions/list-proposals.md)
- [List Quotes](actions/list-quotes.md)
- [List Sent Proposals](actions/list-sent-proposals.md)
- [List Signed Proposals](actions/list-signed-proposals.md)
- [List Templates](actions/list-templates.md)
