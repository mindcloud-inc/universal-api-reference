# Zoho PageSense Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Zoho PageSense expects, and each action page lists the fields available to sort.

## Zoho PageSense actions that support sorting

- [Day-Wise Stats Reports](actions/day-wise-stats-reports.md)
- [Individual Stats Report](actions/individual-stats-report.md)
- [Total Stats Report](actions/total-stats-report.md)
