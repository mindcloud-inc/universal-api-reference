# respond.io Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model respond.io expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/respondio/latest/actions/list-channels?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## respond.io actions that support pagination

- [List Channels](actions/list-channels.md)
- [List Closing Notes](actions/list-closing-notes.md)
- [List Contact Channels](actions/list-contact-channels.md)
- [List Contacts](actions/list-contacts.md)
- [List Custom Fields](actions/list-custom-fields.md)
- [List Message Templates](actions/list-message-templates.md)
- [List Users](actions/list-users.md)
