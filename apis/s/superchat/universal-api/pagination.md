# Superchat Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Superchat expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superchat/latest/actions/list-channels?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Superchat actions that support pagination

- [List Channels](actions/list-channels.md)
- [List Contact Lists](actions/list-contact-lists.md)
- [List Contact Lists for Contact](actions/list-contact-lists-for-contact.md)
- [List Contacts](actions/list-contacts.md)
- [List Contacts for Contact List](actions/list-contacts-for-contact-list.md)
- [List Conversations](actions/list-conversations.md)
- [List Conversations for Contact](actions/list-conversations-for-contact.md)
- [List Custom Attributes](actions/list-custom-attributes.md)
- [List Files](actions/list-files.md)
- [List Inboxes](actions/list-inboxes.md)
- [List Labels](actions/list-labels.md)
- [List Template Folders](actions/list-template-folders.md)
- [List Templates](actions/list-templates.md)
- [List Users](actions/list-users.md)
- [List Webhooks](actions/list-webhooks.md)
- [Search Contacts](actions/search-contacts.md)
