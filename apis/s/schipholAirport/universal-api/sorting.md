# Schiphol Airport Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Schiphol Airport expects, and each action page lists the fields available to sort.

## Schiphol Airport actions that support sorting

- [List Aircraft Types](actions/list-aircraft-types.md)
- [List Airlines](actions/list-airlines.md)
- [List Destinations](actions/list-destinations.md)
- [List Flights](actions/list-flights.md)
