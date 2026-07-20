# PBX Yeastar Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format PBX Yeastar expects, and each action page lists the fields available to sort.

## PBX Yeastar actions that support sorting

- [Query Company Contact List](actions/query-company-contact-list.md)
- [Query Extension List](actions/query-extension-list.md)
- [Query Phonebook List](actions/query-phonebook-list.md)
- [Query Queue List](actions/query-queue-list.md)
- [Query Trunk List](actions/query-trunk-list.md)
- [Search Company Contacts](actions/search-company-contacts.md)
- [Search Extensions](actions/search-extensions.md)
- [Search Phonebooks](actions/search-phonebooks.md)
- [Search Queues](actions/search-queues.md)
- [Search Trunks](actions/search-trunks.md)
