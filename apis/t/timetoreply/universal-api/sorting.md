# Timetoreply Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Timetoreply expects, and each action page lists the fields available to sort.

## Timetoreply actions that support sorting

- [Get Group Mailboxes Report](actions/get-group-mailboxes-report.md)
- [Get Teams Report](actions/get-teams-report.md)
- [List Contact Groups](actions/list-contact-groups.md)
- [List Contacts](actions/list-contacts.md)
- [List Conversation Logs](actions/list-conversation-logs.md)
- [List Group Mailboxes](actions/list-group-mailboxes.md)
- [List Mailboxes](actions/list-mailboxes.md)
- [List Message Logs](actions/list-message-logs.md)
- [List Teams](actions/list-teams.md)
- [List Users](actions/list-users.md)
