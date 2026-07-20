# pixx.io Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format pixx.io expects, and each action page lists the fields available to sort.

## pixx.io actions that support sorting

- [Download Keywords CSV](actions/download-keywords-csv.md)
- [Download Synonyms CSV](actions/download-synonyms-csv.md)
- [List Collections](actions/list-collections.md)
- [List Custom Metadata](actions/list-custom-metadata.md)
- [List Direct Links](actions/list-direct-links.md)
- [List Directories](actions/list-directories.md)
- [List Directory Tree](actions/list-directory-tree.md)
- [List External Shares](actions/list-external-shares.md)
- [List File States](actions/list-file-states.md)
- [List Files](actions/list-files.md)
- [List Keywords](actions/list-keywords.md)
- [List Permission Groups](actions/list-permission-groups.md)
- [List Synonyms](actions/list-synonyms.md)
- [List Upload Links](actions/list-upload-links.md)
- [List Users](actions/list-users.md)
