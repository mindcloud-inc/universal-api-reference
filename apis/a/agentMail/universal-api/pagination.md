# Agent Mail Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Agent Mail expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/list-drafts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Agent Mail actions that support pagination

- [List Drafts](actions/list-drafts.md)
- [List Inbox Drafts](actions/list-inbox-drafts.md)
- [List Inbox List Entries](actions/list-inbox-list-entries.md)
- [List Inbox Messages](actions/list-inbox-messages.md)
- [List Inbox Threads](actions/list-inbox-threads.md)
- [List Inboxes](actions/list-inboxes.md)
- [List Threads](actions/list-threads.md)
- [List Webhooks](actions/list-webhooks.md)
