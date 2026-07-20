# Influenza and Covid-19 Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Influenza and Covid-19 expects, and each action page lists the fields available to sort.

## Influenza and Covid-19 actions that support sorting

- [List Emergency Department Respiratory Daily](actions/list-emergency-department-respiratory-daily.md)
- [List Emergency Department Visits by Demographic Category](actions/list-emergency-department-visits-by-demographic-category.md)
- [List Provisional Respiratory Death Percentages](actions/list-provisional-respiratory-death-percentages.md)
- [List Viral Respiratory Test Positivity](actions/list-viral-respiratory-test-positivity.md)
