# Teamdeck Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Teamdeck expects, and each action page lists the fields available to sort.

## Teamdeck actions that support sorting

- [List Bookings](actions/list-bookings.md)
- [List Projects](actions/list-projects.md)
- [List Resources](actions/list-resources.md)
- [List Time Entries](actions/list-time-entries.md)
- [List Vacations](actions/list-vacations.md)
