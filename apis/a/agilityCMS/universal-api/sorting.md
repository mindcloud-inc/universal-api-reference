# Agility CMS Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Agility CMS expects, and each action page lists the fields available to sort.

## Agility CMS actions that support sorting

- [List Categories (Fetch)](actions/list-categories-fetch.md)
- [List Categories (Preview)](actions/list-categories-preview.md)
- [List Content Items (Fetch)](actions/list-content-items-fetch.md)
- [List Content Items (Preview)](actions/list-content-items-preview.md)
- [List Content Items V1 (Fetch)](actions/list-content-items-v1-fetch.md)
- [List Content Items V1 (Preview)](actions/list-content-items-v1-preview.md)
- [List Posts (Fetch)](actions/list-posts-fetch.md)
- [List Posts (Preview)](actions/list-posts-preview.md)
