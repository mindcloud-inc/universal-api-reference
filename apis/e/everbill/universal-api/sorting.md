# Everbill Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Everbill expects, and each action page lists the fields available to sort.

## Everbill actions that support sorting

- [List Article Categories](actions/list-article-categories.md)
- [List Articles](actions/list-articles.md)
- [List Bills](actions/list-bills.md)
- [List Cost Units](actions/list-cost-units.md)
- [List Customers](actions/list-customers.md)
- [List Distributors](actions/list-distributors.md)
- [List Incoming Bills](actions/list-incoming-bills.md)
- [List Offers](actions/list-offers.md)
- [List Orders](actions/list-orders.md)
- [List Projects](actions/list-projects.md)
