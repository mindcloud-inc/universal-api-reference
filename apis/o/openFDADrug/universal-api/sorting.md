# openFDA Drug Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format openFDA Drug expects, and each action page lists the fields available to sort.

## openFDA Drug actions that support sorting

- [Search Drug Adverse Event Records](actions/search-drug-adverse-event-records.md)
- [Search Drug Enforcement Records](actions/search-drug-enforcement-records.md)
- [Search Drug Label Records](actions/search-drug-label-records.md)
- [Search Drug NDC Records](actions/search-drug-ndc-records.md)
- [Search Drug Shortage Records](actions/search-drug-shortage-records.md)
- [Search Drugs@FDA Records](actions/search-drugs-fda-records.md)
