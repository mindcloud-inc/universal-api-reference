# Instantly Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Instantly expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Instantly actions that support pagination

- [List Accounts](actions/list-accounts.md)
- [List Campaigns](actions/list-campaigns.md)
- [List Emails](actions/list-emails.md)
- [List Lead Lists](actions/list-lead-lists.md)
- [List Webhooks](actions/list-webhooks.md)
