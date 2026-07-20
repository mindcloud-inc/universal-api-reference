# Cakemail Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Cakemail expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cakemail/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Cakemail actions that support pagination

- [List Campaigns](actions/list-campaigns.md)
- [List Contact Tags](actions/list-contact-tags.md)
- [List Contacts](actions/list-contacts.md)
- [List Lists](actions/list-lists.md)
- [List Senders](actions/list-senders.md)
- [Show Email Activity Logs](actions/show-email-activity-logs.md)
