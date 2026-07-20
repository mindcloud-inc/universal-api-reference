# ServiceM8 Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format ServiceM8 expects, and each action page lists the fields available to sort.

## ServiceM8 actions that support sorting

- [List Clients](actions/list-clients.md)
- [List Company Contacts](actions/list-company-contacts.md)
- [List Job Activities](actions/list-job-activities.md)
- [List Job Allocations](actions/list-job-allocations.md)
- [List Jobs](actions/list-jobs.md)
- [List Staff Members](actions/list-staff-members.md)
- [List Tasks](actions/list-tasks.md)
