# 4HSE Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format 4HSE expects, and each action page lists the fields available to sort.

## 4HSE actions that support sorting

- [List Action Sessions](actions/list-action-sessions.md)
- [List Action Subscriptions](actions/list-action-subscriptions.md)
- [List Actions](actions/list-actions.md)
- [List Certificate Action Links](actions/list-certificate-action-links.md)
- [List Certificates](actions/list-certificates.md)
- [List Equipment](actions/list-equipment.md)
- [List Incidents](actions/list-incidents.md)
- [List Offices](actions/list-offices.md)
- [List People](actions/list-people.md)
- [List PersonOffice Assignments](actions/list-person-office-assignments.md)
- [List Projects](actions/list-projects.md)
- [List Session Subscriptions](actions/list-session-subscriptions.md)
- [List Work Groups](actions/list-work-groups.md)
