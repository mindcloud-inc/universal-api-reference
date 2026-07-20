# MailoPost Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model MailoPost expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## MailoPost actions that support pagination

- [List Campaigns](actions/list-campaigns.md)
- [List Email Templates](actions/list-email-templates.md)
- [List Message Webhooks](actions/list-message-webhooks.md)
- [List Organizations](actions/list-organizations.md)
- [List Recipient Lists](actions/list-recipient-lists.md)
- [List Recipients](actions/list-recipients.md)
- [List Segments](actions/list-segments.md)
- [Search Recipients](actions/search-recipients.md)
