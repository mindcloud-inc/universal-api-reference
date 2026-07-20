# Request Tracker (RT) Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Request Tracker (RT) expects, and each action page lists the fields available to sort.

## Request Tracker (RT) actions that support sorting

- [Get Group Members](actions/get-group-members.md)
- [Get Ticket Attachments](actions/get-ticket-attachments.md)
- [Get Ticket History](actions/get-ticket-history.md)
- [Get User Groups](actions/get-user-groups.md)
- [List Queues](actions/list-queues.md)
- [Search Groups](actions/search-groups.md)
- [Search Queues](actions/search-queues.md)
- [Search Tickets](actions/search-tickets.md)
- [Search Users](actions/search-users.md)
