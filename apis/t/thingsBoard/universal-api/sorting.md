# ThingsBoard Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format ThingsBoard expects, and each action page lists the fields available to sort.

## ThingsBoard actions that support sorting

- [List Alarms](actions/list-alarms.md)
- [List Asset Infos](actions/list-asset-infos.md)
- [List Customer Infos](actions/list-customer-infos.md)
- [List Dashboards](actions/list-dashboards.md)
- [List Device Infos](actions/list-device-infos.md)
