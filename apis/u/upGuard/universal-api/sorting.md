# UpGuard Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format UpGuard expects, and each action page lists the fields available to sort.

## UpGuard actions that support sorting

- [List Onboarding Requests](actions/list-onboarding-requests.md)
- [List Vendor Domains](actions/list-vendor-domains.md)
- [List Vendor IPs](actions/list-vendor-ips.md)
