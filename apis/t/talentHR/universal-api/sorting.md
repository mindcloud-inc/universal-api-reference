# TalentHR Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format TalentHR expects, and each action page lists the fields available to sort.

## TalentHR actions that support sorting

- [List Candidates](actions/list-candidates.md)
- [List Employee Assets](actions/list-employee-assets.md)
- [List Employee Completed Tasks](actions/list-employee-completed-tasks.md)
- [List Employee Pending Tasks](actions/list-employee-pending-tasks.md)
- [List Employee Time Off Requests](actions/list-employee-time-off-requests.md)
- [List Job Position Applicants](actions/list-job-position-applicants.md)
