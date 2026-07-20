# Bulldog-WP Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Bulldog-WP expects, and each action page lists the fields available to sort.

## Bulldog-WP actions that support sorting

- [Get campaigns](actions/get-campaigns.md)
- [Search chat messages](actions/get-chat-messages.md)
- [Search chats](actions/get-device-chats.md)
- [List contacts](actions/get-device-contacts.md)
- [Get numbers](actions/get-devices.md)
- [Search files](actions/search-files.md)
- [Search messages](actions/search-messages.md)
