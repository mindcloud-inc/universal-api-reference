# Webex Interact Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Webex Interact expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/filter-shortlinks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Webex Interact actions that support pagination

- [Filter shortlinks](actions/filter-shortlinks.md)
- [List contact lists](actions/list-contact-lists.md)
- [List contacts in list](actions/list-contacts-in-list.md)
- [List scheduled SMS by created date range](actions/list-scheduled-sms-by-created-date-range.md)
- [List scheduled SMS by scheduled date range](actions/list-scheduled-sms-by-scheduled-date-range.md)
- [List senders](actions/list-senders.md)
