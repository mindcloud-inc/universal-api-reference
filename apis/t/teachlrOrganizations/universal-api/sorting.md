# Teachlr Organizations Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Teachlr Organizations expects, and each action page lists the fields available to sort.

## Teachlr Organizations actions that support sorting

- [List Active Courses](actions/list-active-courses.md)
- [List All Non-Expired Courses](actions/list-all-non-expired-courses.md)
- [List Deactivated Courses](actions/list-deactivated-courses.md)
- [List Draft Courses](actions/list-draft-courses.md)
- [List Pending Courses](actions/list-pending-courses.md)
- [List Public Library Courses](actions/list-public-library-courses.md)
