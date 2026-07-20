# Campaign Refinery Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Campaign Refinery expects, and each action page lists the fields available to sort.

## Campaign Refinery actions that support sorting

- [Get Attribute Groups](actions/get-attribute-groups.md)
- [Get Attributes](actions/get-attributes.md)
- [Get Contacts](actions/get-contacts.md)
- [Get Forms](actions/get-forms.md)
- [Get Goals](actions/get-goals.md)
- [Get Tags](actions/get-tags.md)
