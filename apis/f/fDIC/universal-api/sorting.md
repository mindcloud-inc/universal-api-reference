# FDIC Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format FDIC expects, and each action page lists the fields available to sort.

## FDIC actions that support sorting

- [List Bank Failures](actions/list-bank-failures.md)
- [List Financial Institutions](actions/list-financial-institutions.md)
- [List Historical Aggregate Data](actions/list-historical-aggregate-data.md)
- [List Institution Financials](actions/list-institution-financials.md)
- [List Institution Locations](actions/list-institution-locations.md)
- [List Structure Change Events](actions/list-structure-change-events.md)
- [List Summary Of Deposits](actions/list-summary-of-deposits.md)
